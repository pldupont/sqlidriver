package com.pld.sqli.wrapper;

import com.pld.sqli.wrapper.StatementWrapper;
import com.pld.sqli.wrapper.PreparedStatementWrapper;
import com.pld.sqli.wrapper.ConnectionWrapper;
import mockit.Expectations;
import java.sql.CallableStatement;
import java.sql.Connection;
import java.sql.DatabaseMetaData;
import java.sql.SQLWarning;
import java.sql.Savepoint;
import java.sql.Statement;
import java.util.Map;
import java.util.Properties;
import org.junit.Test;
import static org.junit.Assert.*;
import static mockit.Deencapsulation.*;

/**
 * Test methods in ConnectionWrapper class.
 * @author Pierre-Luc Dupont (pldupont@gmail.com)
 */
public class ConnectionWrapperTest {

    /**
     * Test of createStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateStatement_0args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createStatement();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.createStatement();
        assertTrue(result instanceof StatementWrapper);
    }

    /**
     * Test of prepareStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareStatement_String(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareStatement(sql);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.prepareStatement(sql);
        assertTrue(result instanceof PreparedStatementWrapper);
        String s = getField(result, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of prepareCall method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareCall_String(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareCall(sql);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        CallableStatement prepareCall = instance.prepareCall(sql);
        assertTrue(prepareCall instanceof CallableStatementWrapper);
        String s = getField(prepareCall, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of nativeSQL method, of class ConnectionWrapper.
     */
    @Test
    public void testNativeSQL(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.nativeSQL("abc");
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.nativeSQL("abc");
    }

    /**
     * Test of setAutoCommit method, of class ConnectionWrapper.
     */
    @Test
    public void testSetAutoCommit(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setAutoCommit(true);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setAutoCommit(true);
    }

    /**
     * Test of getAutoCommit method, of class ConnectionWrapper.
     */
    @Test
    public void testGetAutoCommit(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getAutoCommit();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getAutoCommit();
    }

    /**
     * Test of commit method, of class ConnectionWrapper.
     */
    @Test
    public void testCommit(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.commit();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.commit();
    }

    /**
     * Test of rollback method, of class ConnectionWrapper.
     */
    @Test
    public void testRollback_0args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.rollback();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.rollback();
    }

    /**
     * Test of close method, of class ConnectionWrapper.
     */
    @Test
    public void testClose(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.close();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.close();
    }

    /**
     * Test of isClosed method, of class ConnectionWrapper.
     */
    @Test
    public void testIsClosed(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.isClosed();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.isClosed();
    }

    /**
     * Test of getMetaData method, of class ConnectionWrapper.
     */
    @Test
    public void testGetMetaData(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getMetaData();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getMetaData();
    }

    /**
     * Test of setReadOnly method, of class ConnectionWrapper.
     */
    @Test
    public void testSetReadOnly(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setReadOnly(true);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setReadOnly(true);
    }

    /**
     * Test of isReadOnly method, of class ConnectionWrapper.
     */
    @Test
    public void testIsReadOnly(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.isReadOnly();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.isReadOnly();
    }

    /**
     * Test of setCatalog method, of class ConnectionWrapper.
     */
    @Test
    public void testSetCatalog(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setCatalog("abc");
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setCatalog("abc");
    }

    /**
     * Test of getCatalog method, of class ConnectionWrapper.
     */
    @Test
    public void testGetCatalog(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getCatalog();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getCatalog();
    }

    /**
     * Test of setTransactionIsolation method, of class ConnectionWrapper.
     */
    @Test
    public void testSetTransactionIsolation(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setTransactionIsolation(10);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setTransactionIsolation(10);
    }

    /**
     * Test of getTransactionIsolation method, of class ConnectionWrapper.
     */
    @Test
    public void testGetTransactionIsolation(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getTransactionIsolation();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getTransactionIsolation();
    }

    /**
     * Test of getWarnings method, of class ConnectionWrapper.
     */
    @Test
    public void testGetWarnings(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getWarnings();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getWarnings();
    }

    /**
     * Test of clearWarnings method, of class ConnectionWrapper.
     */
    @Test
    public void testClearWarnings(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.clearWarnings();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.clearWarnings();
    }

    /**
     * Test of createStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateStatement_int_int(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createStatement(10, 20);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.createStatement(10, 20);
        assertTrue(result instanceof StatementWrapper);
    }

    /**
     * Test of prepareStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareStatement_3args(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareStatement(sql, 10, 20);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.prepareStatement(sql, 10, 20);
        assertTrue(result instanceof PreparedStatementWrapper);
        String s = getField(result, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of prepareCall method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareCall_3args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.prepareCall("abc", 10, 20);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        CallableStatement prepareCall = instance.prepareCall("abc", 10, 20);
        assertNull(prepareCall);
    }

    /**
     * Test of getTypeMap method, of class ConnectionWrapper.
     */
    @Test
    public void testGetTypeMap(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getTypeMap();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getTypeMap();
    }

    /**
     * Test of setTypeMap method, of class ConnectionWrapper.
     */
    @Test
    public void testSetTypeMap(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setTypeMap(null);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setTypeMap(null);
    }

    /**
     * Test of setHoldability method, of class ConnectionWrapper.
     */
    @Test
    public void testSetHoldability(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setHoldability(10);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setHoldability(10);
    }

    /**
     * Test of getHoldability method, of class ConnectionWrapper.
     */
    @Test
    public void testGetHoldability(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getHoldability();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getHoldability();
    }

    /**
     * Test of setSavepoint method, of class ConnectionWrapper.
     */
    @Test
    public void testSetSavepoint_0args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setSavepoint();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setSavepoint();
    }

    /**
     * Test of setSavepoint method, of class ConnectionWrapper.
     */
    @Test
    public void testSetSavepoint_String(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setSavepoint("abc");
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setSavepoint("abc");
    }

    /**
     * Test of rollback method, of class ConnectionWrapper.
     */
    @Test
    public void testRollback_Savepoint(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.rollback((Savepoint) null);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.rollback(null);
    }

    /**
     * Test of releaseSavepoint method, of class ConnectionWrapper.
     */
    @Test
    public void testReleaseSavepoint(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.releaseSavepoint((Savepoint) null);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.releaseSavepoint(null);
    }

    /**
     * Test of createStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateStatement_3args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createStatement(10, 20, 30);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.createStatement(10, 20, 30);
        assertTrue(result instanceof StatementWrapper);
    }

    /**
     * Test of prepareStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareStatement_4args(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareStatement(sql, 10, 20, 30);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.prepareStatement(sql, 10, 20, 30);
        assertTrue(result instanceof PreparedStatementWrapper);
        String s = getField(result, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of prepareCall method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareCall_4args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.prepareCall("abc", 10, 20, 30);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        CallableStatement prepareCall = instance.prepareCall("abc", 10, 20, 30);
        assertNull(prepareCall);
    }

    /**
     * Test of prepareStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareStatement_String_int(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareStatement(sql, 10);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.prepareStatement(sql, 10);
        assertTrue(result instanceof PreparedStatementWrapper);
        String s = getField(result, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of prepareStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareStatement_String_intArr(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareStatement(sql, new int[]{1, 2});
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.prepareStatement(sql, new int[]{1, 2});
        assertTrue(result instanceof PreparedStatementWrapper);
        String s = getField(result, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of prepareStatement method, of class ConnectionWrapper.
     */
    @Test
    public void testPrepareStatement_String_StringArr(final Connection conn) throws Exception {
        final String sql = "fake sql";
        new Expectations() {

            {
                conn.prepareStatement(sql, new String[]{"a", "b"});
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        Statement result = instance.prepareStatement(sql, new String[]{"a", "b"});
        assertTrue(result instanceof PreparedStatementWrapper);
        String s = getField(result, "sql");
        assertEquals(sql, s);
    }

    /**
     * Test of createClob method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateClob(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createClob();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.createClob();
    }

    /**
     * Test of createBlob method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateBlob(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createBlob();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.createBlob();
    }

    /**
     * Test of createNClob method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateNClob(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createNClob();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.createNClob();
    }

    /**
     * Test of createSQLXML method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateSQLXML(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createSQLXML();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.createSQLXML();
    }

    /**
     * Test of isValid method, of class ConnectionWrapper.
     */
    @Test
    public void testIsValid(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.isValid(10);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.isValid(10);
    }

    /**
     * Test of setClientInfo method, of class ConnectionWrapper.
     */
    @Test
    public void testSetClientInfo_String_String(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.setClientInfo("a", "b");
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setClientInfo("a", "b");
    }

    /**
     * Test of setClientInfo method, of class ConnectionWrapper.
     */
    @Test
    public void testSetClientInfo_Properties(final Connection conn) throws Exception {
        final Properties values = new Properties();
        new Expectations() {

            {
                conn.setClientInfo(values);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.setClientInfo(values);
    }

    /**
     * Test of getClientInfo method, of class ConnectionWrapper.
     */
    @Test
    public void testGetClientInfo_String(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getClientInfo("abc");
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getClientInfo("abc");
    }

    /**
     * Test of getClientInfo method, of class ConnectionWrapper.
     */
    @Test
    public void testGetClientInfo_0args(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.getClientInfo();
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.getClientInfo();
    }

    /**
     * Test of createArrayOf method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateArrayOf(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createArrayOf("abc", new Object[]{null});
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.createArrayOf("abc", new Object[]{null});
    }

    /**
     * Test of createStruct method, of class ConnectionWrapper.
     */
    @Test
    public void testCreateStruct(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.createStruct("abc", new Object[]{null});
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.createStruct("abc", new Object[]{null});
    }

    /**
     * Test of unwrap method, of class ConnectionWrapper.
     */
    @Test
    public void testUnwrap(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.unwrap(Object.class);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.unwrap(Object.class);
    }

    /**
     * Test of isWrapperFor method, of class ConnectionWrapper.
     */
    @Test
    public void testIsWrapperFor(final Connection conn) throws Exception {
        new Expectations() {

            {
                conn.isWrapperFor(Object.class);
                times = 1;
            }
        };
        ConnectionWrapper instance = new ConnectionWrapper(conn);
        instance.isWrapperFor(Object.class);
    }
}
