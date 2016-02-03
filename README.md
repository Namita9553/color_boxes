# color_boxes
import java.awt.*;
import java.awt.event.*;
/*<applet code=ColorBoxes width=300 height=300></applet>*/
public class ColorBoxes extends java.applet.Applet 
{ 
	void delay(int time)
		{
			for(int i =1;i<=time;i++);
		}
		public void paint(Graphics g) 
		{
			
			int rval, gval, bval;
			String tempDelay = "20";//getParameter("delay");
			int finalDelay = Integer.parseInt(tempDelay);
			for (int k = 1;k<=100;k++)
			{
				for (int j = 30; j < (size().height -25); j += 30)
				for (int i = 5; i < (size().width -25); i += 30) 
				{
					rval = (int)Math.floor(Math.random() * 256);
					gval = (int)Math.floor(Math.random() * 256);
					bval = (int)Math.floor(Math.random() * 256);
					g.setColor(new Color(rval,gval,bval));
					g.fillRect(i, j, 25, 25);
					g.setColor(Color.black);
					g.drawRect(i, j, 25, 25);
				};
				delay(finalDelay);
			}; 
			
		};
}
