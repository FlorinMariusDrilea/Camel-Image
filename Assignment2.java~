//aca17fmd
import sheffield.*;

public class Assignment2 { 
	public static void main(String[] args){
		EasyReader file=new EasyReader("camel.txt");
		
		//declare constants, create a graphic and declare two 2D arrays of 180
		final int WIDTH=720;
		final int HEIGHT=360;
		EasyGraphics g=new EasyGraphics(WIDTH,HEIGHT);
		
		//arrays used to store the characters from the file
		//used to transfer them from characters to unicode
		char[][] myArray=new char[180][180];
		int [][] intArray=new int[180][180];
		
		//create randomStars between 15-25		
		int randomStars = (int)(Math.random()*25 +10);
		
		//read char from file and convert to int	
		for(int i=0;i<180;i++)
		{
			for(int j=0;j<180;j++)
			{
				myArray[i][j]=file.readChar();
				intArray[i][j]=(int)myArray[i][j];
			}		
		}
		
		//reading the unicode of the characters and put them as pixels of 2x2
		//with the help of some conditions		
		for(int i=0;i<180;i++)
		{
			for(int j=0;j<180;j++)
			{
				
				//draw camel if the character has an even Unicode
				if(intArray[i][j]%2==0)
		        	{                                       
		        		g.setColor(0,255,0);
		        		g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
		        		g.setColor(0,255,0);
		        		g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2);
				    }
				    
				//draw grass if the character has an odd Unicode that is
				//divisible by three
			    else if(intArray[i][j]%2!=0 && intArray[i][j]%3==0)
				    {
				    	g.setColor(255,0,0);
				    	g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
				    	g.setColor(255,0,0);
				    	g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2);
				    }
				   
				//draw background + stars + horizontal horizon
				else
					{  
						int randomizer = (int)(Math.random()*1000 +0);
						int randomizer2 = (int)(Math.random()*1000 +0);
						
						//draw horizontal line at about a third of the way up	
					    if(i>=HEIGHT/3 && j>=0)
					    {
					    	g.setColor(50,100,50);                            
					    	g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
					    	g.setColor(50,100,50);
					        g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2);
					    }
					         
					    //draw random stars on the sky between 10-25 in random
					    //position
					    
					    else 
					    {	
					    	//draw the black background   	
					    	if(randomizer!=1 && randomizer2!=1)
					    	{
					    		g.setColor(0,0,0);
					            g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
					       	    g.setColor(0,0,0);
					            g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2);
					        }
					       
					        //the next 2 steps draw the stars starting with a
					        //random number between 10 and 25, then decreasing
					        //1 of it until randomStars is equal to 0			        
					        else if(randomizer==1 & randomStars!=0)
					        {
					        	g.setColor(255,255,102);
					        	g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
					        	g.setColor(0,0,0);
					        	g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2); 
					            randomStars--;
					        }
					        
					        else if(randomizer2==1 & randomStars!=0)
					        {
					        	g.setColor(0,0,0);
					        	g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
					        	g.setColor(255,255,102);
					            g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2); 
					            randomStars--;
					        }
					        
					        //draw the pixels that remains white with black
					        //color as the background		        
					        else
					        {
					        	g.setColor(0,0,0);
					        	g.fillRectangle(2*j+HEIGHT,HEIGHT-2*i-2,2,2);
					        	g.setColor(0,0,0);
					        	g.fillRectangle(HEIGHT-j*2,HEIGHT-2*i-2,2,2); 
					        }
					    }
					}  	    
			}
			System.out.println();
		}	
	}
}
