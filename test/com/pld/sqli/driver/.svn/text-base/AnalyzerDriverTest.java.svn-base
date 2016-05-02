package com.pld.sqli.driver;

import java.io.File;
import com.pld.sqli.config.SQLIAnalyzerConfig;
import com.pld.sqli.wrapper.ConnectionWrapper;
import java.io.IOException;
import java.util.logging.Logger;
import mockit.Expectations;
import java.sql.Driver;
import java.sql.Connection;
import java.util.Properties;
import java.util.logging.Level;
import org.junit.Test;
import static org.junit.Assert.*;
import static mockit.Deencapsulation.*;

/**
 * Test methods in AnalyzerDriver class.
 * @author Pierre-Luc Dupont (pldupont@gmail.com)
 */
public class AnalyzerDriverTest {
    
    /**
     * Test of initialize method, of class AnalyzerDriver.
     */
    @Test
    public void testInitialize() throws IOException {
        // default initialization
        setField(AnalyzerDriver.class, "initialized", false);
        invoke(AnalyzerDriver.class, "initialize");
        Driver realDriver = getField(AnalyzerDriver.class, "realDriver");
        assertTrue(realDriver instanceof com.mysql.jdbc.Driver);
        
        // already initialize
        invoke(AnalyzerDriver.class, "initialize");
        realDriver = getField(AnalyzerDriver.class, "realDriver");
        assertTrue(realDriver instanceof com.mysql.jdbc.Driver);
       
        // Archive last file
        File storageFile = new File("./build/SQLIAnalyzer/SQLIAnalyzerDiskStorage.xml");
        storageFile.getParentFile().mkdirs();
        storageFile.createNewFile();
        assertTrue(storageFile.exists());
        setField(AnalyzerDriver.class, "initialized", false);
        invoke(AnalyzerDriver.class, "initialize");
        assertFalse(storageFile.exists());
        
        // File not found.
        new Expectations() {
            Logger log;
            SQLIAnalyzerConfig config;
            {
                SQLIAnalyzerConfig.isLoaded();
                result = false;
                times = 1;
                
                Logger.getLogger(AnalyzerDriver.class.getName());
                result = log;
                times = 1;
                
                log.log(Level.SEVERE, "The SQLIAnalyzer configuration is not loaded properly.");
                times = 1;
            }
        };
        setField(AnalyzerDriver.class, "initialized", false);
        invoke(AnalyzerDriver.class, "initialize");
       
        // Driver invalid
        new Expectations() {
            Logger log;
            SQLIAnalyzerConfig config;
            {
                SQLIAnalyzerConfig.isLoaded();
                result = true;
                times = 1;
                
                SQLIAnalyzerConfig.isAnalyzerUseDiskStorage();
                result = false;
                times = 1;
                
                SQLIAnalyzerConfig.getAnalyzerRealDriver();
                result = "dummy.driver";
                times = 1;
                
                Logger.getLogger(AnalyzerDriver.class.getName());
                result = log;
                times = 1;
                
                log.log(Level.SEVERE, "Unable to load the real driver. Failed with exception.", (Throwable) any);
                times = 1;
            }
        };
        setField(AnalyzerDriver.class, "initialized", false);
        invoke(AnalyzerDriver.class, "initialize");
    }

    /**
     * Test of connect method, of class AnalyzerDriver.
     */
    @Test
    public void testConnect(final Driver driver) throws Exception {
        AnalyzerDriver instance = new AnalyzerDriver();
        setField(AnalyzerDriver.class, "realDriver", driver);
        
        new Expectations() {
            SQLIAnalyzerConfig config;
            {
                SQLIAnalyzerConfig.getAnalyzerRealJdbc();
                result = "junit";
                times = 1;

                driver.connect("jdbc:junit://localhost:3306/sqliDriver", (Properties) any);
                times = 1;
                
                SQLIAnalyzerConfig.isAnalyzerActive();
                result = false;
                times = 1;
            }
        };
        Connection result = instance.connect("jdbc:sqli://localhost:3306/sqliDriver", new Properties());
        assertFalse(result instanceof ConnectionWrapper);
        
        new Expectations() {
            SQLIAnalyzerConfig config;
            {
                SQLIAnalyzerConfig.getAnalyzerRealJdbc();
                result = "junit";
                times = 1;

                driver.connect("jdbc:junit://localhost:3306/sqliDriver", (Properties) any);
                times = 1;
                
                SQLIAnalyzerConfig.isAnalyzerActive();
                result = true;
                times = 1;
            }
        };
        result = instance.connect("jdbc:sqli://localhost:3306/sqliDriver", new Properties());
        assertTrue(result instanceof ConnectionWrapper);
    }

    /**
     * Test of acceptsURL method, of class AnalyzerDriver.
     */
    @Test
    public void testAcceptsURL(final Driver driver) throws Exception {
        AnalyzerDriver instance = new AnalyzerDriver();
        setField(AnalyzerDriver.class, "realDriver", driver);

        new Expectations() {
            SQLIAnalyzerConfig config;
            {
                SQLIAnalyzerConfig.getAnalyzerRealJdbc();
                result = "junit";
                times = 1;

                driver.acceptsURL("jdbc:junit://localhost:3306/sqliDriver");
                result = true;
                times = 1;

                SQLIAnalyzerConfig.getAnalyzerRealJdbc();
                result = "junit";
                times = 1;

                driver.acceptsURL("jdbc:junit://localhost:3306/sqliDriver");
                result = false;
                times = 1;
            }
        };
        assertTrue(instance.acceptsURL("jdbc:sqli://localhost:3306/sqliDriver"));
        assertFalse(instance.acceptsURL("jdbc:sqli://localhost:3306/sqliDriver"));
        assertFalse(instance.acceptsURL("jdbc:junit://localhost:3306/sqliDriver"));
    }

    /**
     * Test of getPropertyInfo method, of class AnalyzerDriver.
     */
    @Test
    public void testGetPropertyInfo(final Driver driver) throws Exception {
        new Expectations() {
            {
                driver.getPropertyInfo("abc", (Properties) any);
                times = 1;
            }
        };
        AnalyzerDriver instance = new AnalyzerDriver();
        setField(AnalyzerDriver.class, "realDriver", driver);
        instance.getPropertyInfo("abc", new Properties());
    }

    /**
     * Test of getMajorVersion method, of class AnalyzerDriver.
     */
    @Test
    public void testGetMajorVersion(final Driver driver) throws Exception {
        new Expectations() {
            {
                driver.getMajorVersion();
                times = 1;
            }
        };
        AnalyzerDriver instance = new AnalyzerDriver();
        setField(AnalyzerDriver.class, "realDriver", driver);
        instance.getMajorVersion();
    }

    /**
     * Test of getMinorVersion method, of class AnalyzerDriver.
     */
    @Test
    public void testGetMinorVersion(final Driver driver) throws Exception {
        new Expectations() {
            {
                driver.getMinorVersion();
                times = 1;
            }
        };
        AnalyzerDriver instance = new AnalyzerDriver();
        setField(AnalyzerDriver.class, "realDriver", driver);
        instance.getMinorVersion();
    }

    /**
     * Test of jdbcCompliant method, of class AnalyzerDriver.
     */
    @Test
    public void testJdbcCompliant(final Driver driver) throws Exception {
        new Expectations() {
            {
                driver.jdbcCompliant();
                times = 1;
            }
        };
        AnalyzerDriver instance = new AnalyzerDriver();
        setField(AnalyzerDriver.class, "realDriver", driver);
        instance.jdbcCompliant();
    }
}
