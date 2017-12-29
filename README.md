# Frame_With_Buttons
a piece of code that displays a frame with few buttons on it

    package grouplayout;

    import javax.swing.*;
    import java.awt.*;

    public class Main extends JFrame {

    public Main()
    {
        super("This is a frame with buttons");
        this.setBounds(300,300,300,300);
        this.setIconImage(Toolkit.getDefaultToolkit().getImage("image.png"));
        initComponents();
        this.setResizable(false);
        this.setDefaultCloseOperation(3);
    }
    
    public void initComponents()
    {
        GroupLayout layout = new GroupLayout(getContentPane());
        this.getContentPane().setLayout(layout);
        
        layout.setAutoCreateGaps(true);
        layout.setAutoCreateContainerGaps(true);
        
        layout.setHorizontalGroup(
                layout.createSequentialGroup()
                .addComponent(button1)
                .addGroup(
                layout.createParallelGroup().addComponent(button2).addComponent(button4)
                )
                .addComponent(button3)
                .addContainerGap(10, Short.MAX_VALUE)
                .addComponent(bAnuluj)
                
        );
        
        layout.setVerticalGroup(
                layout.createSequentialGroup()
                .addGroup(
                layout.createParallelGroup().addComponent(button1).addComponent(button2).addComponent(button3)
                )
                .addComponent(button4)
                .addContainerGap(10, Short.MAX_VALUE)
                .addComponent(bAnuluj)
        );
        
        
         this.pack();
    }
    
        JButton button1 = new JButton("Button 1");
        JButton button2 = new JButton("Button 2");
        JButton button3 = new JButton("Button 3");
        JButton button4 = new JButton("Button 4");
        JButton bAnuluj = new JButton("Anuluj");
   
    public static void main(String[] args) {
       
        new Main().setVisible(true);
        
    }
    
    }
