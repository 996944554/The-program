# The-program
import java.util.*;//引用util包

public class Yunsuan {

	public static void main(String[] args)  {
		// TODO Auto-generated method stub
		Random ran = new Random();//初始化随机数
		int num1;
		int num2;
		int num3;
		int num4;
		int chars;
		int num0;
		while(true)
		{
			System.out.println("输入题目的数量：");
			Scanner sca = new Scanner(System.in);
			num0 = sca.nextInt();//输入题数
			System.out.println("真分数运算(1)，整数运算(0)：");
			int  judge = sca.nextInt();
			if(judge == 0)
				for(int i=0; i<num0; i++)
				{
					int k = i+1;
					num1 = ran.nextInt(100);
					num2 = ran.nextInt(100);
					chars = ran.nextInt(4);
					if(chars == 0)
						System.out.println("["+k+"]"+num1+"+"+num2+"=");
					if(chars == 1)
						System.out.println("["+k+"]"+num1+"-"+num2+"=");
					if(chars == 2)
						System.out.println("["+k+"]"+num1+"*"+num2+"=");
					if(chars == 3)
						if(num2 == 0)
							i=i-1;
						else
							System.out.println("["+k+"]"+num1+"/"+num2+"=");
					
				}
			else if(judge == 1)
				for(int i=0; i<num0; i++)
				{
					int k = i+1;
					int t;
					num1 = ran.nextInt(100);
					num2 = ran.nextInt(100);
					num3 = ran.nextInt(100);
					num4 = ran.nextInt(100);
					chars = ran.nextInt(4);
					if(num1>num2)
					{
						t = num2;
						num2 = num1;
						num1 = t;
					}
					if(num1 == num2)
						num2 = num2+1;
					if(num3>num4)
					{
						t = num4;
						num4 = num3;
						num3 = t;
					}
					if(num3 == num4)
						num4 = num4+1;
					if(chars == 0)
						System.out.println("["+k+"]"+num1+"/"+num2+"+"+num3+"/"+num4+"=");
					if(chars == 1)
						System.out.println("["+k+"]"+num1+"/"+num2+"-"+num3+"/"+num4+"=");
					if(chars == 2)
						System.out.println("["+k+"]("+num1+"/"+num2+")*("+num3+"/"+num4+")=");
					if(chars == 3)
						System.out.println("["+k+"]("+num1+"/"+num2+")/("+num3+"/"+num4+")=");
					
				}
			else
				System.out.println("输入有误，请重新");
		}
	}

}
