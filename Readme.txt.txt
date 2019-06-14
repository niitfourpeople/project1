A
PROJECT REPORT
ON
STUDENTS¡¯ MANAGEMENT
SYSTEM


Submitted
By





(Team Name | Individual Name)
Four people | Shi Zhengyang£¨R8J9400016£©
       | Yao Caoge£¨R8J9400013£©
          | Wang Hanneng£¨R8J9400007£©
        | Li Shaopeng£¨R8J9400025£©
 
Start date:2019/05/01
End date:2019/05/16
PROJECT INDEX

S no	Particulars	Page no
1	Project Report Cover	01
2	Project Index	02
3	Team Description & Overview	03
4	Certificate	04
5	Acknowledgement 	05
6	Project Brief	06~08
7	Use case Diagram	09~10
8	Snapshots
Login module
Registration module
Select Module
Search Module
Updata Module
Delete Module
Add Module	
10
11~12
13
13
14
14
15
9	Code of Program
Code of Fame1.java
Code of NewClass,java
Code of NewRoot.java
Code of Newuser.java
Code of delete_1.java
Code of fine,java
Code of updata,java
Code of welcome.java	
15~20
20~21
21~26
26~35
35~39
39~45
45~54
54~60








TEAM DESCRIPTION & OVERVIEW
Our project team is composed of a group of energetic college students who are innovative, share common goals and professional backgrounds. Different interest of a few young people together to the same goal, different people's strengths through cooperation together allow everyone to play each and every one of the biggest advantages, along with the advancement of the project schedule at the same time we will also introduce new promote the development of the project, injected fresh blood to the team, guarantee the group always keeps innovation consciousness and vitality. 
Our team is made up of four people, so it is called Four People.
The members are Yao Caoge, Shi Zhengyang, Wang Hanneng and Li Shaopeng.









CERTIFICATE





















ACKNOWLEDGEMENT
First of all, We would like to thank Hainan University for giving us the opportunity to complete this project.
      We wish to express our sincere thanks to Principal of the college, for providing us with all the necessary facilities.
      We place on record, our sincere gratitude to our teacher, for his constant encouragement.
      We also thank Lecturer, Department of Software Engineering we are extremely grateful and indebted to him for his expert, sincere and valuable guidance and encouragement extended to us.
      We take this opportunity to record our sincere thanks to all the teachers of the Department of ----- for their help and encouragement, we also thank our parents for their unceasing encouragement and support.
      We also place on record, our sense of gratitude to one and all who, directly or indirectly, have lent their helping hand in this venture.








PROJECT REPORT

STUDENTS¡¯ MANAGEMENT
SYSTEM
Student information management system is aimed at the personnel department of a large number of business school work and the development of management software, is mainly used in the school student information management, overall mission is to realize the student information relationship of systematic and scientific, standardization and automation, and its main task is to use a computer to the student daily management for all kinds of information, such as query, modify, add, delete, student information management system is designed for these requirements. The application of school information management system is an important measure to further promote the standardization, electronicalization, control dropouts and improve the level of compulsory education.
This system mainly applies to the school student information management, the overall task is to realize the student information systematization, standardization and automation, its main task is to calculate the student each kind of information carries on the daily management, like inquires, the revision, the increase, the deletion, has designed the student information management system according to these requirements.
As the size of the school continues to grow too large, the number of students has increased dramatically, and the amount of information about students has multiplied. In the face of a large amount of information needs to have a student information management system to improve the efficiency of student management. Through such a system can achieve standardized information management, scientific statistics and rapid query, modification, increase, delete, and so on, so as to reduce the workload of management.
Software Requirements
?	MySQL
?	Any IDE like Eclipse3.2 or NetBeans 5.1
Current situation of student information management system
The management of student information files is of great importance to school administrators. Student information is a very important data resource of colleges and universities and an indispensable part of an educational unit. Especially in recent years, the adjustment of national policies and the large-scale expansion of enrollment in colleges and universities in China have brought a lot of impact on the teaching management, student management, logistics management and other aspects of colleges and universities. It contains large amount of data, the surface of the people involved, and needs to be updated in a timely manner, it is more complicated and difficult to simply rely on manual management, and the traditional artificial management way is neither easy to standardization, management efficiency is not high also, at present our country each kind of colleges and universities there are quite a few students file management still stays on the basis of the paper quality, especially for students in primary and secondary schools of archives management is backward, the management system already can not adapt to the requirement of times development, its management methods will waste a lot of manpower and material resources. With the continuous improvement of science and technology, computer science and technology is becoming more and more mature, the popularity of computer application has entered the various fields of human social life, and is playing an increasingly important role. This traditional manual management mode will inevitably be replaced by computer - based information management method.
Business analysis
This system takes the student information management as the center, the student information may divide into the basic information, the curriculum information. The system can achieve the classification of student information management, at the same time students can also log into the system for their own personal information query.
Functional requirements analysis
Based on the business analysis and the needs of system users, the system needs to achieve the following functions:
(1) administrator: the main functions are: teacher management, student management, course management, password modification and other functions. Among them, the teacher management can carry on the maintenance to the teacher information, may realize to the teacher basic information inquiry, the revision and the deletion, may also add the teacher. Student management is divided into student information maintenance, and the addition of new students, student information maintenance, can achieve the basic information of students query, delete and modify.
(2) teachers: the main functions are: inquiry of teachers' basic information, student achievement management, and password modification. The student achievement management, may inquire this teacher to teach the curriculum student's result, and student's result input.
(3) students: main functions: basic information query, score query, password modification.
The following modules can be identified in our project:
?	Login module
?	Registration module
?	Delete module
?	Search module
?	Update module
?	Select module
Login module
This module makes sure that all access to the system is proper and authenticated. All the links and navigation paths are available for manipulating any kink of information only after an authorized person enters a valid set of user ID and PASSWORD. So this module serve as an entry point for the system and only the authorized person can access it.
Registration module
The module provides an interface to input information for new users. Adding information once can also be edited. All information about user files is stored. The summary information includes fields such as name, grade, address, ID, etc.
Delete module
This module provides an interface for administrators to delete user information. By searching for the student's ID, all information about the student's file is deleted.
Search module
This module provides an interface for users to delete user information. By searching for student ID, all information about student information will be deleted.
Update module
This module provides an interface for administrators to update user information. By searching for student ID, all information about student information will be modified.
Select module
This module provides users with an interface for choosing different options. Different interface modules are accessed by clicking different buttons.



















Use Case diagram
entity-relationship model 
The whole conceptual model of the system can be obtained by analyzing the relations among the entities of the system. 
The E-R diagram of the student entity is shown in the figure:
 
The administrator entity E-R diagram is shown in Figure.
 
Design of System Management Module.
 

Login module
 
Registration module
 
 
 
 
Select Module
 
Search Module
 
Updata Module
 
Delete Module
 
Add Module
 


Code of Program
Code of Fame1.java

package my_project;

import java.sql.*;
import javax.swing.*;
import java.awt.*;

public class Frame1 extends javax.swing.JFrame {  
        String databaseURL = "jdbc:mysql://localhost:3306/student";
        String user = "root";
        String passwords = "1234";
        String driverName = "com.mysql.jdbc.Driver";
        PreparedStatement pst;
        ResultSet rs;
        Connection con;
    public Frame1() {
        initComponents();
        setLocationRelativeTo(null);
        getContentPane().setBackground(Color.orange);
        
    }

   
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        u1 = new javax.swing.JTextField();
        p1 = new javax.swing.JPasswordField();
        exit = new javax.swing.JButton();
        Check = new javax.swing.JButton();
        jLabel4 = new javax.swing.JLabel();
        jButton1 = new javax.swing.JButton();
        jLabel3 = new javax.swing.JLabel();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);
        getContentPane().setLayout(new org.netbeans.lib.awtextra.AbsoluteLayout());

        jLabel1.setFont(new java.awt.Font("Ó×Ô²", 1, 18)); // NOI18N
        jLabel1.setText("Username");
        getContentPane().add(jLabel1, new org.netbeans.lib.awtextra.AbsoluteConstraints(120, 160, -1, -1));

        jLabel2.setFont(new java.awt.Font("Ó×Ô²", 1, 18)); // NOI18N
        jLabel2.setText("Password");
        getContentPane().add(jLabel2, new org.netbeans.lib.awtextra.AbsoluteConstraints(120, 220, -1, -1));

        u1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                u1ActionPerformed(evt);
            }
        });
        getContentPane().add(u1, new org.netbeans.lib.awtextra.AbsoluteConstraints(230, 160, 200, -1));
        getContentPane().add(p1, new org.netbeans.lib.awtextra.AbsoluteConstraints(230, 220, 199, -1));

        exit.setText("Exit");
        exit.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                exitActionPerformed(evt);
            }
        });
        getContentPane().add(exit, new org.netbeans.lib.awtextra.AbsoluteConstraints(310, 310, 120, -1));

        Check.setText("Check");
        Check.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                CheckActionPerformed(evt);
            }
        });
        getContentPane().add(Check, new org.netbeans.lib.awtextra.AbsoluteConstraints(120, 310, 120, -1));

        jLabel4.setFont(new java.awt.Font("Á¥Êé", 1, 24)); // NOI18N
        jLabel4.setText("Administrator login screen");
        getContentPane().add(jLabel4, new org.netbeans.lib.awtextra.AbsoluteConstraints(120, 40, -1, -1));

        jButton1.setText("New User");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });
        getContentPane().add(jButton1, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 350, 90, 20));

        jLabel3.setIcon(new javax.swing.ImageIcon(getClass().getResource("/my_project/µÇÂ½½çÃæ.PNG"))); // NOI18N
        jLabel3.setText("fsadf");
        getContentPane().add(jLabel3, new org.netbeans.lib.awtextra.AbsoluteConstraints(0, 0, 530, 390));

        pack();
    }// </editor-fold>                        

    private void exitActionPerformed(java.awt.event.ActionEvent evt) {                                     
        System.exit(0);
    }                                    

    private void CheckActionPerformed(java.awt.event.ActionEvent evt) {                                      
    
       try{
       Class.forName("com.mysql.jdbc.Driver");
       con=DriverManager.getConnection(databaseURL, user, passwords);
       if(con!=null)
       {
           System.out.println("Connected to the database");
       }
   }
   catch(Exception ex)
   {
       System.out.println("could not find database driver class");
   }     
        if (evt.getSource() == Check) {
            try {
                Class.forName(driverName);
                Connection con = DriverManager.getConnection(databaseURL, user, passwords);
                String sql = "select * from teacher_info where username=? and pw=?";
                pst = con.prepareStatement(sql);
                pst.setString(1, u1.getText());
                pst.setString(2, p1.getText());
                rs = pst.executeQuery();
                if (u1.getText().length() == 0) {
                    JOptionPane.showMessageDialog(this, "Empty User Name", "Warning", JOptionPane.WARNING_MESSAGE);
                } else if (p1.getPassword().length == 0) {
                    JOptionPane.showMessageDialog(this, "Empty Password", "Warning", JOptionPane.WARNING_MESSAGE);
                } else if (rs.next()) {
                    welcome s = new welcome();
                    s.setVisible(true);
                    dispose();
                } else {
                    JOptionPane.showMessageDialog(this, "Incorre User Name or Password", "Error", JOptionPane.ERROR_MESSAGE);
                }
            } catch (Exception e) {
                JOptionPane.showMessageDialog(this, e);
            }
        }   
    }                                     

    private void u1ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        // TODO add your handling code here:
    }                                  

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        NewRoot n=new NewRoot();
        n.show();
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /*
         * Set the Nimbus look and feel
         */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /*
         * If Nimbus (introduced in Java SE 6) is not available, stay with the
         * default look and feel. For details see
         * http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(Frame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(Frame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(Frame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(Frame1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /*
         * Create and display the form
         */
        java.awt.EventQueue.invokeLater(new Runnable() {

            public void run() {
                new Frame1().setVisible(true);
            }
        });
    }
    // Variables declaration - do not modify                     
    private javax.swing.JButton Check;
    private javax.swing.JButton exit;
    private javax.swing.JButton jButton1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JLabel jLabel4;
    private javax.swing.JPasswordField p1;
    private javax.swing.JTextField u1;
    // End of variables declaration                   
}

Code of NewClass,java
package my_project;
import java.sql.*;
public class NewClass 
 {
    static private Connection connection;
    public static Connection getConnection() throws Exception
    {
    if(connection==null)
    {
    Class.forName("com.mysql.jdbc.Driver");
    connection=DriverManager.getConnection("jdbc:mysql://localhost:3306/student", "root", "1234");
    }
    return connection;
    }
}

Code of NewRoot.java
/*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */
package my_project;

import java.sql.*;
import javax.swing.JOptionPane;

/**
 *
 * @author »ªË¶
 */
public class NewRoot extends javax.swing.JFrame {

    /**
     * Creates new form NewRoot
     */
    public NewRoot() {
        initComponents();
        setLocationRelativeTo(null);
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jLabel1 = new javax.swing.JLabel();
        un = new javax.swing.JTextField();
        jLabel2 = new javax.swing.JLabel();
        jLabel3 = new javax.swing.JLabel();
        pw = new javax.swing.JTextField();
        jButton1 = new javax.swing.JButton();
        jButton2 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jLabel1.setFont(new java.awt.Font("ËÎÌå", 0, 24)); // NOI18N
        jLabel1.setText("New Root");

        jLabel2.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 0, 18)); // NOI18N
        jLabel2.setText("Username:");

        jLabel3.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 0, 18)); // NOI18N
        jLabel3.setText("Passwords:");

        jButton1.setText("Ok");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        jButton2.setText("Back");
        jButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton2ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGap(143, 143, 143)
                        .addComponent(jLabel1))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(63, 63, 63)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                            .addComponent(jLabel2, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                            .addComponent(jLabel3, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
                        .addGap(32, 32, 32)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            .addComponent(un, javax.swing.GroupLayout.PREFERRED_SIZE, 100, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(pw, javax.swing.GroupLayout.PREFERRED_SIZE, 100, javax.swing.GroupLayout.PREFERRED_SIZE)))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(72, 72, 72)
                        .addComponent(jButton2, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(94, 94, 94)
                        .addComponent(jButton1, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)))
                .addContainerGap(94, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(21, 21, 21)
                .addComponent(jLabel1)
                .addGap(34, 34, 34)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(un, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel2))
                .addGap(41, 41, 41)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jLabel3)
                    .addComponent(pw, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 54, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jButton1)
                    .addComponent(jButton2))
                .addGap(48, 48, 48))
        );

        pack();
    }// </editor-fold>                        

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        try{
        Connection cn=NewClass.getConnection();
        String sql="insert into teacher_info values(?,?)";
        PreparedStatement pst=cn.prepareStatement(sql);
        pst.setString(1,un.getText());
        pst.setString(2,pw.getText());
        int n=pst.executeUpdate();
        if(n>0)
        {
        JOptionPane.showMessageDialog(this,"Insert successfully");
        System.exit(0);
        }
        }catch(Exception e)
        {
        System.out.println(e);
        }
    }                                        

    private void jButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        System.exit(0);
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /*
         * Set the Nimbus look and feel
         */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /*
         * If Nimbus (introduced in Java SE 6) is not available, stay with the
         * default look and feel. For details see
         * http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(NewRoot.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(NewRoot.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(NewRoot.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(NewRoot.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /*
         * Create and display the form
         */
        java.awt.EventQueue.invokeLater(new Runnable() {

            public void run() {
                new NewRoot().setVisible(true);
            }
        });
    }
    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JButton jButton2;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JTextField pw;
    private javax.swing.JTextField un;
    // End of variables declaration                   
}

Code of Newuser.java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package my_project;


import java.awt.Color;
import java.sql.*;
import javax.swing.JOptionPane;

/**
 *
 * @author ÍõººÄÜ
 */
public class Newuser extends javax.swing.JFrame {

    /**
     * Creates new form newuser
     */
    public Newuser() {
        initComponents();
        setLocationRelativeTo(null);
    
       
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        jLabel3 = new javax.swing.JLabel();
        jLabel4 = new javax.swing.JLabel();
        jLabel7 = new javax.swing.JLabel();
        jLabel8 = new javax.swing.JLabel();
        jLabel11 = new javax.swing.JLabel();
        jLabel12 = new javax.swing.JLabel();
        jLabel13 = new javax.swing.JLabel();
        n5 = new javax.swing.JTextField();
        n2 = new javax.swing.JTextField();
        n3 = new javax.swing.JTextField();
        n8 = new javax.swing.JTextField();
        n1 = new javax.swing.JTextField();
        n6 = new javax.swing.JTextField();
        n4 = new javax.swing.JTextField();
        n7 = new javax.swing.JTextField();
        jLabel15 = new javax.swing.JLabel();
        submit = new javax.swing.JButton();
        jButton1 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jLabel1.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 36)); // NOI18N
        jLabel1.setText("Please add information for a new student");

        jLabel2.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel2.setText("id");

        jLabel3.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel3.setText("address");

        jLabel4.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel4.setText("name");

        jLabel7.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel7.setText("major");

        jLabel8.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel8.setText("class");

        jLabel11.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel11.setText("College Chinese");

        jLabel12.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel12.setText("higher mathematics");

        jLabel13.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel13.setText("college English ");

        n5.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                n5ActionPerformed(evt);
            }
        });

        n8.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                n8ActionPerformed(evt);
            }
        });

        n1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                n1ActionPerformed(evt);
            }
        });

        jLabel15.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 24)); // NOI18N
        jLabel15.setText(" Essential information:");

        submit.setFont(new java.awt.Font("ËÎÌå", 0, 14)); // NOI18N
        submit.setText("Submit");
        submit.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                submitActionPerformed(evt);
            }
        });

        jButton1.setFont(new java.awt.Font("ËÎÌå", 0, 14)); // NOI18N
        jButton1.setText("Back");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGap(118, 118, 118)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            .addComponent(jLabel4)
                            .addComponent(jLabel2)
                            .addComponent(jLabel3)
                            .addComponent(jLabel7))
                        .addGap(27, 27, 27)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            .addComponent(n1, javax.swing.GroupLayout.PREFERRED_SIZE, 149, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(n2, javax.swing.GroupLayout.PREFERRED_SIZE, 149, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(n3, javax.swing.GroupLayout.PREFERRED_SIZE, 149, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(n4, javax.swing.GroupLayout.PREFERRED_SIZE, 149, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addGap(22, 22, 22)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.TRAILING)
                            .addComponent(jLabel11)
                            .addComponent(jLabel8)
                            .addComponent(jLabel12)
                            .addComponent(jLabel13)))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(227, 227, 227)
                        .addComponent(jButton1, javax.swing.GroupLayout.PREFERRED_SIZE, 77, javax.swing.GroupLayout.PREFERRED_SIZE)))
                .addGap(51, 51, 51)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(submit, javax.swing.GroupLayout.PREFERRED_SIZE, 87, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                        .addComponent(n6)
                        .addComponent(n5, javax.swing.GroupLayout.DEFAULT_SIZE, 149, Short.MAX_VALUE)
                        .addComponent(n7)
                        .addComponent(n8)))
                .addGap(0, 0, Short.MAX_VALUE))
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addComponent(jLabel15, javax.swing.GroupLayout.PREFERRED_SIZE, 279, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addContainerGap())
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addGap(0, 73, Short.MAX_VALUE)
                        .addComponent(jLabel1)
                        .addGap(91, 91, 91))))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jLabel1)
                .addGap(45, 45, 45)
                .addComponent(jLabel15)
                .addGap(67, 67, 67)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(n1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel2)
                    .addComponent(jLabel8)
                    .addComponent(n5, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(53, 53, 53)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jLabel4)
                    .addComponent(n2, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel11)
                    .addComponent(n6, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(58, 58, 58)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jLabel3)
                    .addComponent(n3, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jLabel12)
                    .addComponent(n7, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGap(67, 67, 67)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(jLabel7)
                            .addComponent(n4, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                            .addComponent(jLabel13))
                        .addContainerGap())
                    .addGroup(layout.createSequentialGroup()
                        .addGap(63, 63, 63)
                        .addComponent(n8, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 79, Short.MAX_VALUE)
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                            .addComponent(submit)
                            .addComponent(jButton1))
                        .addGap(60, 60, 60))))
        );

        pack();
    }// </editor-fold>                        

    private void n5ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        // TODO add your handling code here:
    }                                  

    private void n1ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        // TODO add your handling code here:
    }                                  

    private void n8ActionPerformed(java.awt.event.ActionEvent evt) {                                   
        // TODO add your handling code here:
    }                                  

    private void submitActionPerformed(java.awt.event.ActionEvent evt) {                                       
         try {
Connection cn=NewClass.getConnection();
String sql="INSERT INTO student_info VALUES(?,?,?,?,?,?,?,?)";
PreparedStatement pdt=cn.prepareStatement(sql);
pdt.setString(1,n1.getText());
pdt.setString(2,n2.getText());
pdt.setString(3, n3.getText());
pdt.setString(4, n4.getText());
pdt.setString(5, n5.getText());
pdt.setString(6, n6.getText());
pdt.setString(7, n7.getText());
pdt.setString(8, n8.getText());
int n=pdt.executeUpdate();
if(n>0)
{
JOptionPane.showMessageDialog(this,"Insert successfully");
System.exit(0);
}
}catch(Exception e)
{
System.out.println(e);
}
    }                                      

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
      welcome w=new welcome();
      w.show();
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(Newuser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(Newuser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(Newuser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(Newuser.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new Newuser().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel11;
    private javax.swing.JLabel jLabel12;
    private javax.swing.JLabel jLabel13;
    private javax.swing.JLabel jLabel15;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JLabel jLabel4;
    private javax.swing.JLabel jLabel7;
    private javax.swing.JLabel jLabel8;
    private javax.swing.JTextField n1;
    private javax.swing.JTextField n2;
    private javax.swing.JTextField n3;
    private javax.swing.JTextField n4;
    private javax.swing.JTextField n5;
    private javax.swing.JTextField n6;
    private javax.swing.JTextField n7;
    private javax.swing.JTextField n8;
    private javax.swing.JButton submit;
    // End of variables declaration                   
}

Code of delete_1.java
/*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */
package my_project;

import java.io.*;
import java.sql.*;
import java.util.*;
import javax.swing.*;

/**
 *
 * @author 7570
 */
public class delete_1 extends javax.swing.JFrame {

    public delete_1() {
        initComponents();
        setLocationRelativeTo(null);
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jl = new javax.swing.JLabel();
        jt = new javax.swing.JTextField();
        jb1 = new javax.swing.JButton();
        jb2 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jl.setFont(new java.awt.Font("Ó×Ô²", 1, 18)); // NOI18N
        jl.setText("Enter the ID you want to delete");

        jb1.setText("delete");
        jb1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jb1ActionPerformed(evt);
            }
        });

        jb2.setText("exit");
        jb2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jb2ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(46, 46, 46)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addComponent(jb1)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                        .addComponent(jb2)
                        .addGap(83, 83, 83))
                    .addGroup(layout.createSequentialGroup()
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addComponent(jl)
                            .addComponent(jt, javax.swing.GroupLayout.PREFERRED_SIZE, 172, javax.swing.GroupLayout.PREFERRED_SIZE))
                        .addContainerGap())))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(29, 29, 29)
                .addComponent(jl)
                .addGap(45, 45, 45)
                .addComponent(jt, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(67, 67, 67)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jb1)
                    .addComponent(jb2))
                .addContainerGap(100, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void jb2ActionPerformed(java.awt.event.ActionEvent evt) {                                    
        welcome w=new welcome();
        w.show();
    }                                   

    private void jb1ActionPerformed(java.awt.event.ActionEvent evt) {                                    

        try {

            Connection con = NewClass.getConnection();
            String sql = "delete from student_info where id=?";
            PreparedStatement ps = con.prepareStatement(sql);
            ps.setString(1, jt.getText());
            int rs = ps.executeUpdate();

            if (rs != 0) {
                JOptionPane.showMessageDialog(this,"you are deleted");
            }
            else{
                JOptionPane.showMessageDialog(this,"Incorrect id","Error",JOptionPane.ERROR_MESSAGE);
            }
        } catch (Exception e) {
            JOptionPane.showMessageDialog(this,e);
        }

    }                                   

    public static void main(String args[]) {
        /*
         * Set the Nimbus look and feel
         */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /*
         * If Nimbus (introduced in Java SE 6) is not available, stay with the
         * default look and feel. For details see
         * http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(delete_1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(delete_1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(delete_1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(delete_1.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /*
         * Create and display the form
         */
        java.awt.EventQueue.invokeLater(new Runnable() {

            public void run() {
                new delete_1().setVisible(true);
            }
        });
    }
    // Variables declaration - do not modify                     
    private javax.swing.JButton jb1;
    private javax.swing.JButton jb2;
    private javax.swing.JLabel jl;
    private javax.swing.JTextField jt;
    // End of variables declaration                   
}

Code of fine,java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package my_project;

import java.sql.Connection;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.ResultSetMetaData;
import javax.swing.JOptionPane;
import javax.swing.table.DefaultTableModel;

/**
 *
 * @author ÍõººÄÜ
 */
public class fine extends javax.swing.JFrame {
    String[] a;
    /**
     * Creates new form fine
     */
    public fine() {
        initComponents();
         setLocationRelativeTo(null);
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jScrollPane1 = new javax.swing.JScrollPane();
        jTable1 = new javax.swing.JTable();
        search = new javax.swing.JTextField();
        ok = new javax.swing.JButton();
        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        jButton1 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jTable1.setModel(new javax.swing.table.DefaultTableModel(
            new Object [][] {
                {null, null, null, null, null, null, null, null},
                {null, null, null, null, null, null, null, null},
                {null, null, null, null, null, null, null, null},
                {null, null, null, null, null, null, null, null}
            },
            new String [] {
                "Id", "Name", "Address", "Major", "Class", "Chinese", "Math", "null"
            }
        ));
        jScrollPane1.setViewportView(jTable1);

        search.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                searchActionPerformed(evt);
            }
        });

        ok.setFont(new java.awt.Font("ËÎÌå", 0, 18)); // NOI18N
        ok.setText("Search");
        ok.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                okActionPerformed(evt);
            }
        });

        jLabel1.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 0, 24)); // NOI18N
        jLabel1.setText("Search Student Information");

        jLabel2.setFont(new java.awt.Font("ËÎÌå", 0, 18)); // NOI18N
        jLabel2.setText("Input ID:");

        jButton1.setFont(new java.awt.Font("ËÎÌå", 0, 14)); // NOI18N
        jButton1.setText("Back");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addContainerGap(35, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(jLabel2)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(search, javax.swing.GroupLayout.PREFERRED_SIZE, 244, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(60, 60, 60)
                        .addComponent(ok, javax.swing.GroupLayout.PREFERRED_SIZE, 104, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(85, 85, 85))
                    .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                        .addComponent(jButton1)
                        .addGap(78, 78, 78))))
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addGroup(layout.createSequentialGroup()
                        .addGap(25, 25, 25)
                        .addComponent(jScrollPane1))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(141, 141, 141)
                        .addComponent(jLabel1, javax.swing.GroupLayout.PREFERRED_SIZE, 327, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addGap(0, 0, Short.MAX_VALUE)))
                .addContainerGap())
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(javax.swing.GroupLayout.Alignment.TRAILING, layout.createSequentialGroup()
                .addGap(41, 41, 41)
                .addComponent(jLabel1, javax.swing.GroupLayout.PREFERRED_SIZE, 54, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, 54, Short.MAX_VALUE)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(search, javax.swing.GroupLayout.PREFERRED_SIZE, 34, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(ok)
                    .addComponent(jLabel2))
                .addGap(36, 36, 36)
                .addComponent(jScrollPane1, javax.swing.GroupLayout.PREFERRED_SIZE, 173, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(40, 40, 40)
                .addComponent(jButton1)
                .addGap(61, 61, 61))
        );

        pack();
    }// </editor-fold>                        

    private void searchActionPerformed(java.awt.event.ActionEvent evt) {                                       
        // TODO add your handling code here:
    }                                      

    private void okActionPerformed(java.awt.event.ActionEvent evt) {                                   
        try{
            Connection con=NewClass.getConnection();
            String sql3="select * from student_info where id=?";
            PreparedStatement pre=con.prepareStatement(sql3);
            pre.setString(1,search.getText());
            ResultSet res=pre.executeQuery();
            ResultSetMetaData rsmd=res.getMetaData();
            int columnCount=rsmd.getColumnCount();
            DefaultTableModel tm=(DefaultTableModel)jTable1.getModel();
            tm.setColumnCount(0);
            tm.setRowCount(0);
            while(res.next())
            {
            for(int i=1;i<=columnCount;i++)
            {
            tm.addColumn(rsmd.getCatalogName(i));
            a=new String[columnCount];
            for(int s=0;s<columnCount;s++)
            {
            a[s]=res.getString(s+1);
            }
            }
            tm.addRow(a);
            }
            if(search.getText().length()==0)
            {
            JOptionPane.showMessageDialog(this,"Empty User ID","Warning",JOptionPane.WARNING_MESSAGE);
            }
            tm.fireTableDataChanged();
        }catch(Exception e)
        {
       System.out.println(e);
        }
    }                                  

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
        welcome w=new welcome();
        w.show();
    }                                        

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(fine.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(fine.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(fine.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(fine.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new fine().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JScrollPane jScrollPane1;
    private javax.swing.JTable jTable1;
    private javax.swing.JButton ok;
    private javax.swing.JTextField search;
    // End of variables declaration                   
}

Code of updata,java
package my_project;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import javax.swing.JOptionPane;

public class updata extends javax.swing.JFrame {

    public updata() {
        initComponents();
        setLocationRelativeTo(null);
    }

    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jl1 = new javax.swing.JLabel();
        jt1 = new javax.swing.JTextField();
        jl7 = new javax.swing.JLabel();
        jl6 = new javax.swing.JLabel();
        jl2 = new javax.swing.JLabel();
        jl3 = new javax.swing.JLabel();
        jl5 = new javax.swing.JLabel();
        jl4 = new javax.swing.JLabel();
        jt2 = new javax.swing.JTextField();
        jt3 = new javax.swing.JTextField();
        jt7 = new javax.swing.JTextField();
        jt6 = new javax.swing.JTextField();
        jt5 = new javax.swing.JTextField();
        jt4 = new javax.swing.JTextField();
        jLabel12 = new javax.swing.JLabel();
        jb1 = new javax.swing.JButton();
        jb2 = new javax.swing.JButton();
        jl8 = new javax.swing.JLabel();
        jt8 = new javax.swing.JTextField();
        jl = new javax.swing.JLabel();
        jt = new javax.swing.JTextField();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jl1.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl1.setText("ID");
        jl1.setToolTipText("");

        jl7.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl7.setText("English");
        jl7.setToolTipText("");

        jl6.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl6.setText("Math");
        jl6.setToolTipText("");

        jl2.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl2.setText("NAME");
        jl2.setToolTipText("");

        jl3.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl3.setText("MAJOR");
        jl3.setToolTipText("");

        jl5.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl5.setText("Chinese");
        jl5.setToolTipText("");

        jl4.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl4.setText("CLASS");
        jl4.setToolTipText("");

        jLabel12.setFont(new java.awt.Font("Ó×Ô²", 1, 18)); // NOI18N
        jLabel12.setText("GRADE");
        jLabel12.setToolTipText("");

        jb1.setText("ÐÞ¸Ä");
        jb1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jb1ActionPerformed(evt);
            }
        });

        jb2.setText("È¡Ïû");
        jb2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jb2ActionPerformed(evt);
            }
        });

        jl8.setFont(new java.awt.Font("ËÎÌå", 2, 18)); // NOI18N
        jl8.setText("ADDRESS");
        jl8.setToolTipText("");

        jl.setFont(new java.awt.Font("ËÎÌå", 0, 14)); // NOI18N
        jl.setText("ENTER THE ID you want to updata");

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                    .addGroup(layout.createSequentialGroup()
                        .addContainerGap()
                        .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                            .addGroup(layout.createSequentialGroup()
                                .addComponent(jl3, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(jt3, javax.swing.GroupLayout.PREFERRED_SIZE, 83, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(58, 58, 58)
                                .addComponent(jl4, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(4, 4, 4)
                                .addComponent(jt4, javax.swing.GroupLayout.PREFERRED_SIZE, 83, javax.swing.GroupLayout.PREFERRED_SIZE))
                            .addGroup(layout.createSequentialGroup()
                                .addGap(66, 66, 66)
                                .addComponent(jb1)
                                .addGap(96, 96, 96)
                                .addComponent(jb2))
                            .addGroup(layout.createSequentialGroup()
                                .addComponent(jl7, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(jt7, javax.swing.GroupLayout.PREFERRED_SIZE, 72, javax.swing.GroupLayout.PREFERRED_SIZE))
                            .addGroup(layout.createSequentialGroup()
                                .addComponent(jl5, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(jt5, javax.swing.GroupLayout.PREFERRED_SIZE, 72, javax.swing.GroupLayout.PREFERRED_SIZE)
                                .addGap(43, 43, 43)
                                .addComponent(jl6)
                                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                .addComponent(jt6, javax.swing.GroupLayout.PREFERRED_SIZE, 75, javax.swing.GroupLayout.PREFERRED_SIZE))
                            .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING, false)
                                .addGroup(layout.createSequentialGroup()
                                    .addComponent(jl, javax.swing.GroupLayout.PREFERRED_SIZE, 229, javax.swing.GroupLayout.PREFERRED_SIZE)
                                    .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED, javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE)
                                    .addComponent(jt, javax.swing.GroupLayout.PREFERRED_SIZE, 40, javax.swing.GroupLayout.PREFERRED_SIZE))
                                .addGroup(layout.createSequentialGroup()
                                    .addComponent(jl1, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                    .addGap(6, 6, 6)
                                    .addComponent(jt1, javax.swing.GroupLayout.PREFERRED_SIZE, 83, javax.swing.GroupLayout.PREFERRED_SIZE)
                                    .addGap(58, 58, 58)
                                    .addComponent(jl2, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                                    .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                                    .addComponent(jt2, javax.swing.GroupLayout.PREFERRED_SIZE, 83, javax.swing.GroupLayout.PREFERRED_SIZE)))))
                    .addGroup(layout.createSequentialGroup()
                        .addGap(154, 154, 154)
                        .addComponent(jLabel12, javax.swing.GroupLayout.PREFERRED_SIZE, 98, javax.swing.GroupLayout.PREFERRED_SIZE))
                    .addGroup(layout.createSequentialGroup()
                        .addContainerGap()
                        .addComponent(jl8, javax.swing.GroupLayout.PREFERRED_SIZE, 70, javax.swing.GroupLayout.PREFERRED_SIZE)
                        .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                        .addComponent(jt8)))
                .addContainerGap(104, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addGap(10, 10, 10)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jl)
                    .addComponent(jt, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(18, 18, 18)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jl1)
                    .addComponent(jt1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jt2, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jl2))
                .addGap(18, 18, 18)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jt3, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jl3)
                    .addComponent(jt4, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jl4))
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.UNRELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jl8)
                    .addComponent(jt8, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(9, 9, 9)
                .addComponent(jLabel12)
                .addPreferredGap(javax.swing.LayoutStyle.ComponentPlacement.RELATED)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.BASELINE)
                    .addComponent(jl5)
                    .addComponent(jt5, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                    .addComponent(jl6)
                    .addComponent(jt6, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(10, 10, 10)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jl7)
                    .addComponent(jt7, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE))
                .addGap(18, 18, 18)
                .addGroup(layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jb2)
                    .addComponent(jb1))
                .addContainerGap(23, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void jb1ActionPerformed(java.awt.event.ActionEvent evt) {                                    
        try {
            Connection con = NewClass.getConnection();
            String sql = "update student_info set id=?,name=?,major=?,class=?,address=?,yu=?,shu=?,wai=? where id=?";
            PreparedStatement ps = con.prepareStatement(sql);
            ps.setString(9, jt.getText());
            ps.setString(1, jt1.getText());
            ps.setString(2, jt2.getText());
            ps.setString(3, jt3.getText());
            ps.setString(4, jt4.getText());
            ps.setString(5, jt5.getText());
            ps.setString(6, jt6.getText());
            ps.setString(7, jt7.getText());
            ps.setString(8, jt8.getText());

            int rs = ps.executeUpdate();

            if (rs != 0) {
                JOptionPane.showMessageDialog(this, "you are successed");
            } else {
                JOptionPane.showMessageDialog(this, "Iyou are wrong", "Error", JOptionPane.ERROR_MESSAGE);
            }

        } catch (Exception e) {
            JOptionPane.showMessageDialog(this, e);
        }
    }                                   

    private void jb2ActionPerformed(java.awt.event.ActionEvent evt) {                                    
        welcome w=new welcome();
         w.show();
    }                                   

    public static void main(String args[]) {

        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /*
         * If Nimbus (introduced in Java SE 6) is not available, stay with the
         * default look and feel. For details see
         * http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(updata.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(updata.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(updata.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(updata.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>


        java.awt.EventQueue.invokeLater(new Runnable() {

            public void run() {
                new updata().setVisible(true);
            }
        });
    }
    // Variables declaration - do not modify                     
    private javax.swing.JLabel jLabel12;
    private javax.swing.JButton jb1;
    private javax.swing.JButton jb2;
    private javax.swing.JLabel jl;
    private javax.swing.JLabel jl1;
    private javax.swing.JLabel jl2;
    private javax.swing.JLabel jl3;
    private javax.swing.JLabel jl4;
    private javax.swing.JLabel jl5;
    private javax.swing.JLabel jl6;
    private javax.swing.JLabel jl7;
    private javax.swing.JLabel jl8;
    private javax.swing.JTextField jt;
    private javax.swing.JTextField jt1;
    private javax.swing.JTextField jt2;
    private javax.swing.JTextField jt3;
    private javax.swing.JTextField jt4;
    private javax.swing.JTextField jt5;
    private javax.swing.JTextField jt6;
    private javax.swing.JTextField jt7;
    private javax.swing.JTextField jt8;
    // End of variables declaration                   
}

Code of welcome.java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

package my_project;

import java.sql.Connection;

/**
 *
 * @author ÍõººÄÜ
 */
public class welcome extends javax.swing.JFrame {

    /**
     * Creates new form Welcome
     */
    public welcome() {
        initComponents();
         setLocationRelativeTo(null);
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jLabel2 = new javax.swing.JLabel();
        jLabel3 = new javax.swing.JLabel();
        jToggleButton1 = new javax.swing.JToggleButton();
        jToggleButton2 = new javax.swing.JToggleButton();
        jToggleButton3 = new javax.swing.JToggleButton();
        jToggleButton4 = new javax.swing.JToggleButton();
        jButton1 = new javax.swing.JButton();
        jLabel1 = new javax.swing.JLabel();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);
        getContentPane().setLayout(new org.netbeans.lib.awtextra.AbsoluteLayout());

        jLabel2.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 36)); // NOI18N
        jLabel2.setText("Welcom£¡");
        getContentPane().add(jLabel2, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 10, -1, -1));

        jLabel3.setFont(new java.awt.Font("Î¢ÈíÑÅºÚ", 1, 18)); // NOI18N
        jLabel3.setText("You can do the following£º");
        getContentPane().add(jLabel3, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 80, -1, -1));

        jToggleButton1.setText("²é¿´Ñ§ÉúÐÅÏ¢£¨To fine the information of students£©");
        jToggleButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jToggleButton1ActionPerformed(evt);
            }
        });
        getContentPane().add(jToggleButton1, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 150, 490, 70));

        jToggleButton2.setText("Ìí¼ÓÑ§ÉúÐÅÏ¢£¨To add the information of students£©");
        jToggleButton2.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jToggleButton2ActionPerformed(evt);
            }
        });
        getContentPane().add(jToggleButton2, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 260, 490, 70));

        jToggleButton3.setText("ÐÞ¸ÄÑ§ÉúÐÅÏ¢£¨To alter the information of students£©");
        jToggleButton3.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jToggleButton3ActionPerformed(evt);
            }
        });
        getContentPane().add(jToggleButton3, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 370, 490, 70));

        jToggleButton4.setText("É¾³ýÑ§ÉúÐÅÏ¢£¨To delete the information of students£©");
        jToggleButton4.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jToggleButton4ActionPerformed(evt);
            }
        });
        getContentPane().add(jToggleButton4, new org.netbeans.lib.awtextra.AbsoluteConstraints(10, 480, 490, 70));

        jButton1.setText("ESC");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });
        getContentPane().add(jButton1, new org.netbeans.lib.awtextra.AbsoluteConstraints(700, 510, 110, 40));

        jLabel1.setIcon(new javax.swing.ImageIcon(getClass().getResource("/my_project/»¶Ó­½çÃæ.jpg"))); // NOI18N
        getContentPane().add(jLabel1, new org.netbeans.lib.awtextra.AbsoluteConstraints(0, 0, 860, 570));

        pack();
    }// </editor-fold>                        

    private void jToggleButton3ActionPerformed(java.awt.event.ActionEvent evt) {                                               
       try{
       Connection con=NewClass.getConnection();
       updata al=new updata();
       al.setVisible(true);
       dispose();}catch(Exception e)
       {
       System.out.println(e);
       }
        // TODO add your handling code here:
    }                                              

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
       try{
        Connection con=NewClass.getConnection();
       Frame1 f3=new Frame1();
        f3.show();
        this.hide();}
       catch(Exception e)
       {
       System.out.println(e);
       }
        // TODO add your handling code here:
    }                                        

    private void jToggleButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                               
      try{ 
       Connection con=NewClass.getConnection();
        fine f=new fine();
       f.setVisible(true);
       dispose();}
      catch(Exception e)
      {
      System.out.println(e);
      }
        // TODO add your handling code here:
    }                                              

    private void jToggleButton2ActionPerformed(java.awt.event.ActionEvent evt) {                                               
     
        try{
       Connection con=NewClass.getConnection();
       Newuser a=new Newuser();
       a.setVisible(true);
       dispose();
        }catch(Exception e)
      {
      System.out.println(e);
      }
        // TODO add your handling code here:
    }                                              

    private void jToggleButton4ActionPerformed(java.awt.event.ActionEvent evt) {                                               
       try{
       Connection con=NewClass.getConnection();
       delete_1 de=new delete_1();
       de.setVisible(true);
       dispose();}
       catch(Exception e)
       {
       System.out.println(e);
       }
        // TODO add your handling code here:
    }                                              

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(welcome.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(welcome.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(welcome.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(welcome.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            @Override
            public void run() {
                new welcome().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabel3;
    private javax.swing.JToggleButton jToggleButton1;
    private javax.swing.JToggleButton jToggleButton2;
    private javax.swing.JToggleButton jToggleButton3;
    private javax.swing.JToggleButton jToggleButton4;
    // End of variables declaration                   
}
