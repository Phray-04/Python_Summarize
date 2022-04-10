# Python GUI —— TKinter

基于Python tkinter与pygame开发飞机大战项目

>小游戏    exe    UI

 Tkinter 模块(Tk 接口)是 Python 的标准 Tk GUI 工具包的接口 .快速构建GUI应用程序


```
#基本的tkinter结构——Hello World
import tkinter
top = tkinter.Tk()
top.mainloop()
```

# Java GUI —— Swing

基于Java Swing开发基本功能模块的GUI测试

> 开发测试UI

```
#基本的swing结构——Hello World
import javax.swing.*;
public class HelloWorldSwing {
    /**{
     * 创建并显示GUI。出于线程安全的考虑，
     * 这个方法在事件调用线程中调用。
     */
    private static void createAndShowGUI() {
        // 确保一个漂亮的外观风格
        JFrame.setDefaultLookAndFeelDecorated(true);

        // 创建及设置窗口
        JFrame frame = new JFrame("HelloWorldSwing");
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // 添加 "Hello World" 标签
        JLabel label = new JLabel("Hello World");
        frame.getContentPane().add(label);

        // 显示窗口
        frame.pack();
        frame.setVisible(true);
    }

    public static void main(String[] args) {
        // 显示应用 GUI
        javax.swing.SwingUtilities.invokeLater(new Runnable() {
            public void run() {
                createAndShowGUI();
            }
        });
    }
}
```

