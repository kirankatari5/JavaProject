import java.util.Random;
import java.util.Scanner;
interface styles
{
	static Scanner sc=new Scanner(System.in);
	static String def="\u001B[0m";
	static String blink="\u001B[5m";
	static String red="\u001B[31m";
	static String green="\u001B[32m";
	static String yellow="\u001B[33m";
	static String blue="\u001B[34m";
	static String purple="\u001B[35m";
	static String skblue="\u001B[36m";
	static String Bold = "\033[0;1m";
	static String airplane = "\u2708"; 
	static String car = "\uD83D\uDE97";
	static String train = "\uD83D\uDE86"; 
	static String ship = "\uD83D\uDEA2"; 
	static String darkBlue = "\u001B[34m";
	static String pink = "\u001B[95m";
	static String darkPink = "\u001B[35m";
	static String cyan="\u001B[36m";
	static String emoji = "\uD83D\uDE00";
	static String space="                                            ";
	static String space1="                                             ";
	static String welcome="                                 ";
	static String welcome1="                                     ";
	static String welcome2="                                   ";
	static String space2="                                                ";
	static String space3="                          ";
}
class Main extends ConfirmPassword implements styles 
{ 


	static
	{
		System.out.println("------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("------------------------------------------------------------------------------------------------------------------------------------------------------------"+"\n");
		System.out.println(Bold+blue+blink+welcome+"\t\t"+"@   @"+"\t"+"@@@@@"+"\t"+"@    "+"\t"+"  @@@"+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@@@@@"+"\t\t"+"@@@@@"+"\t"+"  @  ");
		System.out.println(welcome+"\t\t"+"@   @"+"\t"+"@    "+"\t"+"@    "+"\t"+" @   "+"\t"+"@   @"+"\t"+"@@ @@"+"\t"+"@    "+"\t\t"+"  @  "+"\t"+"@   @");
		System.out.println(welcome+"\t\t"+"@ @ @"+"\t"+"@@@@@"+"\t"+"@    "+"\t"+"@    "+"\t"+"@   @"+"\t"+"@ @ @"+"\t"+"@@@@@"+"\t\t"+"  @  "+"\t"+"@   @");
		System.out.println(welcome+"\t\t"+"@@ @@"+"\t"+"@    "+"\t"+"@    "+"\t"+" @   "+"\t"+"@   @"+"\t"+"@   @"+"\t"+"@    "+"\t\t"+"  @  "+"\t"+"@   @");
		System.out.println(welcome+"\t\t"+"@   @"+"\t"+"@@@@@"+"\t"+"@@@@@"+"\t"+"  @@@"+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@@@@@"+"\t\t"+"  @  "+"\t"+"  @  "+def);
		System.out.println();
		System.out.println(Bold+pink+blink+welcome+"\t\t\t"+"@   @"+"\t"+"  @  "+"\t"+"  @@@"+"\t"+"  @  "+"\t"+"@@@@@"+"\t"+"@@@@@"+"\t"+"  @  "+"\t"+"@   @");
		System.out.println(welcome+"\t\t\t"+"@   @"+"\t"+" @ @ "+"\t"+" @   "+"\t"+" @ @ "+"\t"+"  @  "+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@ @ @");
		System.out.println(welcome+"\t\t\t"+"@   @"+"\t"+"@   @"+"\t"+"@    "+"\t"+"@   @"+"\t"+"  @  "+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@  @@");
		System.out.println(welcome+"\t\t\t"+" @ @ "+"\t"+"@@@@@"+"\t"+" @   "+"\t"+"@@@@@"+"\t"+"  @  "+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@   @");
		System.out.println(welcome+"\t\t\t"+"  @  "+"\t"+"@   @"+"\t"+"  @@@"+"\t"+"@   @"+"\t"+"  @  "+"\t"+"@@@@@"+"\t"+"  @  "+"\t"+"@   @"+def);
		System.out.println();
		System.out.println(Bold+yellow+blink+welcome+"\t\t\t"+"@   @"+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@@@  "+"\t"+"@@@@@"+"\t"+"@@@@ "+"\t"+" @@@@");
		System.out.println(welcome+"\t\t\t"+"@   @"+"\t"+"@   @"+"\t"+"@@  @"+"\t"+"@  @ "+"\t"+"@    "+"\t"+"@   @"+"\t"+"@    ");
		System.out.println(welcome+"\t\t\t"+"@ @ @"+"\t"+"@   @"+"\t"+"@ @ @"+"\t"+"@   @"+"\t"+"@@@@@"+"\t"+"@@@@@"+"\t"+"@@@@@");
		System.out.println(welcome+"\t\t\t"+"@@ @@"+"\t"+"@   @"+"\t"+"@  @@"+"\t"+"@  @ "+"\t"+"@    "+"\t"+"@  @ "+"\t"+"    @");
		System.out.println(welcome+"\t\t\t"+"@   @"+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@@@  "+"\t"+"@@@@@"+"\t"+"@   @"+"\t"+"@@@@ "+def+"\n");
		System.out.println("------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("------------------------------------------------------------------------------------------------------------------------------------------------------------"+"\n");

	}

	void sign_log()
	{
		System.out.println("\n\n\n"+"\t\t\t\t\t\t\t    Select one option for Singup/login "+"\n"+"\t\t\t\t\t\t\t     1. Sign up"+"\n"+"\t\t\t\t\t\t\t     2. Login"+"\n");
		int SL=sc.nextInt();
		switch(SL)
		{
		case 1 :System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			setEmail();
		else
			sign_log();
		break;
		case 2 :System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			login();
		else
			sign_log();
		break;
		default :System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			sign_log();

		}
	}

	String firstname;
	String lastname;
	long phone;
	String gender;
	String email;
	String password;
	String confirmPassword;
	private String stored_Mail="wonders@gmail.com";
	private String stored_Password="1234";
	static Main ob=new Main();

	void setEmail()
	{
		System.out.print("\t\t\t\t\t"+Bold+"ENTER FIRSTNAME				: ");
		this.firstname=sc.next();
		System.out.print("\t\t\t\t\t"+"ENTER LASTNAME				: ");
		this.lastname=sc.next();
		System.out.print("\t\t\t\t\t"+"ENTER MOBILE NUMBER			: ");
		this.phone=sc.nextLong();
		System.out.print("\t\t\t\t\t"+"ENTER GENDER				: ");
		this.gender=sc.next();
		System.out.print("\t\t\t\t\t"+"ENTER YOUR MAIL ID 			: ");
		ob.valid();
		match();
	}
	void match()
	{
		System.out.print("\t\t\t\t\t"+Bold+"CREATE PASSWORD 			: ");
		password=sc.next();
		System.out.print("\t\t\t\t\t"+"CONFIRM YOUR PASSWORD 			: ");
		confirmPassword=sc.next();
		if(password.equals(confirmPassword))
		{
			System.out.println("\t\t\t\t\t"+green+"SUCCESSFULLY SIGNED UP"+def);
			login();
		}
		else
		{
			System.out.println("\t\t\t\t\t"+red+"PASSWORD MISS MATCH"+def);
			System.out.println("\t\t\t\t\t"+yellow+"RE-ENTER YOUR PASSWORD"+def);
			match();
		}
	}
	void valid()
	{
		this.email=sc.next();
		int x=email.length();
		int f=0,e=0,g=0,h=0,j=0,l=0,m=0,k=0;
		for(int i=0;i<=(x-5);i++)
		{
			char c=email.charAt(i);
			if(c=='@')
				e++;
			if(c>='A'&& c<='Z')
				f++;
			if(c>='0' && c<='9')
				g++;
			if(c>='a'&&c<='z')
				j++;
		}
		if(email.charAt(x-4)=='.')
			h++;
		if(email.charAt(x-3)=='c'||email.charAt(x-3)=='C')
			k++;
		if(email.charAt(x-2)=='o'||email.charAt(x-2)=='O')
			l++;
		if(email.charAt(x-1)=='m'||email.charAt(x-1)=='M')
			m++;
		if(e!=0&&(f!=0||j!=0 || g!=0)&&h!=0&&k!=0&&l!=0&&m!=0)
		{
			System.out.println("\t\t\t\t\t"+green+"EMAIL VERIFIED AND CREATE YOUR PASSWORD"+def);
		}
		else
		{
			System.out.println("\t\t\t\t\t"+red+"Invalid"+red);
			System.out.print("\t\t\t\t\t"+Bold+"ENTER YOUR EMAIL ID PROPERLY            : "+def);
			valid();
		}

	}
	void login()
	{
		System.out.print("\t\t\t\t\t"+Bold+"ENTER YOUR EMAIL ID		        : ");
		String email1=sc.next();
		if(email1.equals (this.email))
		{
			System.out.println("\t\t\t\t\t"+green+"TYPE true FOR ENTER PASSWORD "+def+"or "+red+ "FALSE FOR FORGET PASSWORD "+def);
			boolean EPF=sc.nextBoolean();
			if(EPF==true)
			{
				System.out.print("\t\t\t\t\t"+Bold+"ENTER YOUR PASSWORD			: ");
				String password=sc.next();
				if(password.equals(this.password))
				{
					System.out.println("\t\t\t\t\t"+green+"PLEASE WAIT LOGGING IN........"+def);
				}
				else
				{
					System.out.println("\t\t\t\t\t"+red+"Invalid Email Try again...."+def);
					login();
				}
			}
			else{
				forget();
			}
		}
		else if(!email1.equals (this.email))
		{
			System.out.println("\t\t\t\t\t"+red+"Invalid Email Try again...."+def);
			login();
		}
		else if(email1 .equals (stored_Mail))
		{
			System.out.println("\t\t\t\t\t"+green+"TYPE true FOR ENTER PASSWORD "+def+"or "+red+ "FALSE FOR FORGET PASSWORD "+def);
			boolean EPF1=sc.nextBoolean();
			if(EPF1==true)
			{
				System.out.print("\t\t\t\t\t"+Bold+"ENTER YOUR PASSWORD 			: ");
				String password=sc.next();
				if(password.equals(stored_Password))
				{
					System.out.println("PLEASE WAIT LOGGING IN........");
				}
				else 
				{
					login();
				}
			}
			else
			{
				forget();
			}
		}
		else if(!email1.equals (stored_Mail))
		{
			System.out.println("\t\t\t\t\t"+red+"Invalid Email Try again...."+def);
			login();
		}
	}
	String create_Password;
	String confirm_Password;
	void forget()
	{
		System.out.print("\t\t\t\t\t"+Bold+"CREATE NEW PASSWORD			: ");
		create_Password=sc.next();
		System.out.print("\t\t\t\t\t"+"CONFIRM PASSWORD 			: ");
		confirm_Password=sc.next();
		if(password.equals(confirm_Password))
		{
			System.out.println("\t\t\t\t\t"+darkBlue+"YOUR NEW PASSWORD  MATCHED TO THE OLD PASSWRD"+def);
			confirm();
		}
		else if(stored_Password.equals(confirm_Password))
		{
			System.out.println("\t\t\t\t\t"+darkBlue+"YOUR NEW PASSWORD  MATCHED TO THE OLD PASSWRD"+def);
			confirm();
		}
		else{
			System.out.println("\t\t\t\t\t"+green+"NEW PASSWORD CREATED"+def);

			confirm();
		}
	}
	void confirm()
	{
		System.out.print("\t\t\t\t\t"+Bold+"ENTER YOUR EMAIL ID 			: ");
		String email1=sc.next();
		//String password1=confirm_Password;
		System.out.print("\t\t\t\t\t"+Bold+"ENTER YOUR NEW PASSWORD 		: ");
		String em=sc.next();
		if(!em.equals(password)&&em.equals(em))
		{	System.out.println("\t\t\t\t\t"+green+"Please Wait.......Logging in........"+def);
		//System.out.println("YOU HAVE ENTERED YOUR OLD PASSWORD");
		//confirm();
		}	
		/*else if(em.equals(em))
		{
    			System.out.println("\t\t\t\t\t"+green+"Please Wait.......Logging in........"+def);
		}*/
		else if(!em.equals(confirm_Password)&&em.equals(em))
		{
			System.out.println("\t\t\t\t\t"+green+"Please Wait.......Logging in........"+def);
			//System.out.println("YOU HAVE ENTERED YOUR OLD PASSWORD");
			//confirm();	
		}
		else
		{
			System.out.println("\t\t\t\t\t"+red+"Invalid Password"+def);
			confirm();
		}
	}

	static void tour()
	{
		System.out.println(def+"\t\t\t\t\t\t\t\tSelect the region");
		System.out.println("\t\t\t\t\t\t\t\t1.South  2.North");
		int region1=sc.nextInt();
		switch(region1)  
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				south();
			else
				tour();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				north();
			else
				tour();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				tour();
		}
	}
	static void south()
	{
		System.out.println(Bold+skblue+blink+"------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(Bold+skblue+blink+"\t\t\t\t\t\t\t\t**WELCOME TO SOUTH INDIA**");   
		System.out.println("------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(def+"\t\t\t\t\t\t\t    Choose one state from the following");
		System.out.println("\t\t\t\t\t\t\t    1.Telangana 2.AndhraPradesh 3.Kerala");   
		int state=sc.nextInt();
		switch(state)
		{   
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home .equals ("yes"))
				telangana();
			else
				south();
			break; 
		case 2: 
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals ("yes"))
				Andhrapradesh();
			else
				south();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home2=sc.next();
			if(home2.equals ("yes"))
				kerala();
			else
				south();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the state enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				south();

		}  

	}
	static void Andhrapradesh()
	{

		System.out.println(Bold+green+"------------------------------------------------------------------------------------------------------------------------------------------------------------");

		System.out.println("\t\t\t\t\t\t\t        *WELCOME TO Andhra Pradesh*");  
		System.out.println(           "------------------------------------------------------------------------------------------------------------------------------------------------------------");

		System.out.println(darkBlue+"Andhra Pradesh, The south-eastern coastal state of India, Andhra Pradesh is popularly known as the Rice Bowl of India. Endowing to abundant natural marvels, this state attracts a huge number of tourists every year. "+"\n");
		System.out.println(yellow+welcome+"\t      The best time to visit Andhra Pradesh is from November to February");
		System.out.println(welcome2+def+"\t\t\t\tSelect your dream place to visit");
		System.out.println(space2+"\t\t\t1.Visakhapatnam" +"\n"+ space2+"\t\t\t2.Tirupati"+"\n"+ space2+"\t\t\t3.Srisailam" +"\n"+ space2+"\t\t\t4.kurnool " +"\n"+space2+"\t\t\t5.Kakinada");  
		int place=sc.nextInt();
		switch(place)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			Visakhapatnam();
		else
			Andhrapradesh();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			Tirupati();
		else
			Andhrapradesh();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			Srisailam();
		else
			Andhrapradesh();
		break;
		case 4:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home3=sc.next();
		if(home3.equals("yes")||home3.equals("YES"))
			Kurnool();
		else
			Andhrapradesh();
		break;
		case 5:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home4=sc.next();
		if(home4.equals("yes")||home4.equals("YES"))
			Kakinada();
		else
			Andhrapradesh();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back :  ");
		String back=sc.next().toLowerCase();
		if(back==back)
			Andhrapradesh();

		}
	}  
	static void Visakhapatnam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected Visakhapatnam");
		System.out.println(def+space2+" \tPlease make a selection from the below options");
		System.out.println(space2+"\t\t\t1. Near by places" +"\n"+ space2+"\t\t\t2. Famous for " +"\n"+ space2+"\t\t\t3. How to reach");
		int list=sc.nextInt();
		switch(list)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Visakhapatnam();
		else
			Visakhapatnam();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Visakhapatnam();
		else
			Visakhapatnam();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Visakhapatnam();
		else
			Visakhapatnam();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back :  ");
		String back=sc.next().toLowerCase();
		if(back==back)
			Visakhapatnam();
		}
	}
	static void nearby_Visakhapatnam()
	{
		System.out.println(Bold+blue+space2+"\t     Places to Visit Near Visakhapatnam");
		System.out.println(blue+def+space2+"\t\t\t1.Araku Valley"+"\n"+ space2+"\t\t\t2.Borra Caves"+"\n"+space2+"\t\t\t3.Rushikonda Beach"+"\n"+space2+"\t\t\t4.Kailasagiri"+"\n"+space2+"\t\t\t5.Aircraft Museum");

	}
	static void famous_Visakhapatnam()
	{
		System.out.println(welcome1+"Famous Food : 1.Bongu Chicken 2.Tomato Bajji 3.Egg Bonda");

	}
	static void route_Visakhapatnam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");
		int famousl=sc.nextInt();
		switch(famousl)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus_v();
			else
				route_Visakhapatnam();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab_v();
			else
				route_Visakhapatnam();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Visakhapatnam();

		}
	}
	static void bus_v()
	{
		System.out.println("Visakhapatnam: Available Buses are 0019,3418,900R");
	}
	static void cab_v()
	{
		System.out.println("Visakhapatnam: cabs available ");
	}
	static void Tirupati()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected Tirupati");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list1=sc.nextInt();
		switch(list1)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Tirupati();
		else
			Tirupati();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Tirupati();
		else
			Tirupati();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Tirupati();
		else
			Tirupati();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back :  ");
		String back=sc.next().toLowerCase();
		if(back==back)
			Tirupati();
		}
	}
	static void nearby_Tirupati()
	{
		System.out.println(Bold+blue+space2+"\t     Places to Visit Near Tirupati");
		System.out.println(blue+def+space2+"\t\t\t1.Sri Venkateswara Swami Temple"+"\n"+space2+"\t\t\t2.Sri Govindarajaswami Temple"+"\n"+space2+"\t\t\t3.Kapila Teerdam"+"\n"+space2+"\t\t\t4.Sri venkateswara Zoo Park"+"\n"+space2+"\t\t\t5.Chandragiri Fort");

	}
	static void famous_Tirupati()
	{
		System.out.println(welcome1+"Famous Food : 1.Srivari laddu 2.Bisibelebhath 3.Pulihora");

	}
	static void route_Tirupati()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");
		int famous2=sc.nextInt();
		switch(famous2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus_T();
			else
				route_Tirupati();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab_T();
			else
				route_Tirupati();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Tirupati();

		}
	}
	static void bus_T()
	{
		System.out.println("Tirupati: Available Buses are 3547,8615,0813");
	}
	static void cab_T()
	{
		System.out.println("Tirupati: cabs available ");
	}
	static void Srisailam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected Srisailam");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Srisailam();
		else
			Srisailam();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Srisailam();
		else
			Srisailam();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Srisailam();
		else
			Srisailam();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back :  ");
		String back=sc.next().toLowerCase();
		if(back==back)
			Srisailam();
		}
	}
	static void nearby_Srisailam()
	{
		System.out.println(Bold+blue+space2+"\t     Places to Visit Near Srisailam");
		System.out.println(blue+def+space2+"\t\t\t1.Mallikarjuna Swamy Temple"+"\n"+space2+"\t\t\t2.Srisailam dam"+"\n"+space2+"\t\t\t3.Pathala Ganga"+"\n"+space2+"\t\t\t4.Akkamahadevi Caves"+"\n"+space2+"\t\t\t5.Octopus View");

	}
	static void famous_Srisailam()
	{
		System.out.println(welcome1+"Famous Food : 1.laddu 2.Alasandala Vada 3.Raagi Sankati");

	}
	static void route_Srisailam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");
		int famous3=sc.nextInt();
		switch(famous3)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus_S();
			else
				route_Srisailam();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab_S();
			else
				route_Srisailam();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Srisailam();

		}
	}
	static void bus_S()
	{
		System.out.println("Srisailam: Available Buses are 0262,0108,4688");
	}
	static void cab_S()
	{
		System.out.println("Srisailam: cabs available ");
	}
	static void Kurnool()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Kurnool");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Kurnool();
		else
			Kurnool();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Kurnool();
		else
			Kurnool();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Kurnool();
		else
			Kurnool();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back :  ");
		String back=sc.next().toLowerCase();
		if(back==back)
			Kurnool();
		}
	}
	static void nearby_Kurnool()
	{

		System.out.println(Bold+blue+space2+"\t     Places to Visit Near  Kurnool");
		System.out.println(blue+def+space2+"\t\t\t1.Yaganti"+"\n"+space2+"\t\t\t2.Belum Caves"+"\n"+space2+"\t\t\t3.KondaReddy Fort"+"\n"+space2+"\t\t\t4.Kurnool Fort"+"\n"+space2+"\t\t\t5.Archaeological Museum");
	}
	static void famous_Kurnool()
	{
		System.out.println(welcome1+"Famous Food : 1.Ugani Bajji 2.Sajja Roti 3.Mirchi Pakoda");

	}
	static void route_Kurnool()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");
		int famous4=sc.nextInt();
		switch(famous4)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus_KR();
			else
				route_Kurnool();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab_KR();
			else
				route_Kurnool();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Kurnool();

		}
	}
	static void bus_KR()
	{
		System.out.println("Kurnool: Available Buses are 292,0802,0802 ");
	}
	static void cab_KR()
	{
		System.out.println("Kurnool: cabs available ");
	}
	static void Kakinada()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Kakinada");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list=sc.nextInt();
		switch(list)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Kurnool();
		else
			Kurnool();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Kurnool();
		else
			Kurnool();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Kurnool();
		else
			Kurnool();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back :  ");
		String back=sc.next().toLowerCase();
		if(back==back)
			Kakinada();
		}
	}
	static void nearby_Kakinada()
	{
		System.out.println(Bold+blue+space2+"\t     Places to Visit Near Kakinada");
		System.out.println(blue+def+space2+"\t\t\t1.Kakinada Beach"+"\n"+space2+"\t\t\t2.Coringa Wildlife Sanctuary"+"\n"+space2+"\t\t\t3.Hope Island"+"\n"+space2+"\t\t\t4.Draksharamam");

	}
	static void famous_Kakinada()
	{
		System.out.println(welcome1+"Famous Food : 1.kaja 2.Atreyapuram Putarekulu 3.Chandrakanthalu 4.Palakayalu");

	}
	static void route_Kakinada()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");
		int famous5=sc.nextInt();
		switch(famous5)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus_KK();
			else
				route_Kakinada();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab_KK();
			else
				route_Kakinada();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Kakinada();

		}
	}
	static void bus_KK()
	{
		System.out.println("Kakinada: Available Buses are 0154,615,6310");
	}
	static void cab_KK()
	{
		System.out.println("Kakinada: cabs available ");
	}
	static void telangana()
	{
		System.out.println(Bold+green+"------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("\t\t\t\t\t\t\t         *WELCOME TO TELANGANA*");  
		System.out.println(           "------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(darkBlue+"Telangana is a state located in the southern part of India. It was officially formed on June 2, 2014, as the 29th state of India, following a long-standing demand for its separate statehood. Telangana was carved out of the northern region of the state of Andhra Pradesh, and its capital is Hyderabad, one of India's major cities. "+"\n");
		System.out.println(yellow+welcome+"\t         The best time to visit Telangana is from October to March");
		System.out.println(welcome2+def+"\t\t\t\tSelect your dream place to visit");
		System.out.println(space2+"\t\t\t1.ANATHAGIRI" +"\n"+ space2+"\t\t\t2.WARANGAL "+"\n"+ space2+"\t\t\t3.POCHAMPALLY" +"\n"+ space2+"\t\t\t4.BHADHRACHALAM " +"\n"+space2+"\t\t\t5.HYDERABAD ");
		int place = sc.nextInt();
		switch(place)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))

				anathagiri();
			else
				telangana();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				warangal();
			else
				telangana();
			break;
		case 3: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				pochampally();
			else
				telangana();
			break;
		case 4:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES")) 
				Bhadhrachalam();
			else
				telangana();
			break;
		case 5: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home4=sc.next();
			if(home4.equals("yes")||home4.equals("YES"))
				hyderabad();
			else
				telangana();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				telangana();
			System.out.println("YOU HAVE SELECTED WRONG NUMBER");
			//case 5:Tour_package();break;

		}
	}
	static void anathagiri()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Anathagiri");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int An= sc.nextInt();
		switch(An)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))

				placesnearby();
			else
				anathagiri();
			break;
		case 2:System.out.print("Type YES for continue OR type NO to go back: ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))

			famousfood();
		else
			anathagiri();
		break;
		case 3: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))
				route();
			else
				anathagiri();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				anathagiri();


		}
	}
	static void placesnearby()
	{
		System.out.println(Bold+blue+space2+"\t       Places to Visit Near anathagiri");
		System.out.println(blue+def+space2+"\t\t\t1.Chilakur Balaji Temple"+"\n"+space2+"\t\t\t2.Nehru Zoological Park"+"\n"+space2+"\t\t\t3.Vikarabad"+"\n"+space2+"\t\t\t4.Mahabubnagar");
	}
	static void famousfood()
	{
		System.out.println("Famous  food : 1.CHAI 2.SWEETS 3.PULIHORA 4.ANATHAGIRI TEMPLE 5.SCENIC BEAUTY 6. BONICAL GRADENS 7. TYDA PARK 8. NAGALA GUTTA");

	}
	static void famousrest()
	{
		System.out.println("THESE THREE RESTAURANT");
		System.out.println("1. PARADISE RESTAURANT +/n+ 2.BAWARCHI+ /n +3. MINERVA COFFEE SHOP");
		int fam = sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES")) 
				paradise();
			else
				famousrest();
			break;
		case 2: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				bawarchi();
			else
				famousrest();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))
				minerva();
			else
				famousrest();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				famousrest();
		}
	}
	static void paradise()
	{
		System.out.println("PARADISE BIRYANI");   
	}
	static void bawarchi()
	{
		System.out.print("BAWARCHI BIRYANI");
	}
	static void minerva()
	{
		System.out.println("MINERVA");  
	}
	static void route()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.train");          
		//String way = sc.nextInt();
		int fam = sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				buus();
			else
				route();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				train();
			else
				route();
			break;
		default: 
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route();

		}
	}
	static void buus()
	{
		System.out.println("telangana TO chilkur balaji AVALIBLE BUS NO : 1.288S, 2.288R (JBS),(MGBS)");

	}
	static  void train()
	{  
		System.out.println("ANATHAGIRI TO VIKARABAD AVALIBLE TRAIN NO:1.57687,2.(TSRTC)");    
	}
	static void warangal()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Warangal");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int An= sc.nextInt();
		switch(An)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				pplacesnearby();
			else
				warangal();
			break;


		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				famoussfood();
			else
				warangal();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))
				routewarant();
			else
				warangal();
			break;
		default: 
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				warangal();
		}
	}
	static void pplacesnearby()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Warangal");
		System.out.println(blue+def+space2+"\t\t\t1.Thousand Pillar Temple" +"\n"+space2+ "\t\t\t2.Kakatiya Rock Garden" +"\n"+space2+"\t\t\t3.Ramappa Temple"+"\n"+space2+"\t\t\t4.Bhadrakali Temple");          
	}

	static void famoussfood()
	{
		System.out.println("Famous food : 1.CHAI 2.SWEETS 3.PULIHORA ");
	}

	static void routewarant()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Metro");

		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))

				busw();
			else
				routewarant();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				metrow();
			else
				routewarant();
			break;
		default: 
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				routewarant();

		}
	}
	static void busw()
	{
		System.out.println("WARANGAL TO CHILKUR BALALJI AVALIBLE BUSES NO:1. 2. 57687,3. (TSRTC)");        
	}
	static void metrow()
	{
		System.out.println("WARANGAL TO VIKARABAD AVALIBALE  METRO NO:ERHJH3467,RY3Y263727");    
	}
	static void pochampally()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Pochampally");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");

		int An= sc.nextInt();
		switch(An)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))

				place();
			else
				pochampally();
			break;
		case 2: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				famousssfood();
			else
				pochampally();
			break;
		case 3: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES")) 
				routepocham();
			else
				pochampally();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				pochampally();  
		}
	}
	static void place()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Pochampally");
		System.out.println(blue+def+space2+"\t\t\t1.Pochampally Handloom Park" +"\n"+space2+ "\t\t\t2.Yadagri Gutta" +"\n"+space2+"\t\t\t3.Surendrapuri"+"\n"+space2+"\t\t\t4.Kulpakji Jain Temple");         
	}

	static void famousssfood()
	{
		System.out.println("Famous food .: 1.SARVAPENDI 2.MUTTON 3.NATU KODI 4.BAGJI 5.STREET FOOD 6. POCHAMPALLY TKAT SAREES 7. IKAT WEAVING TECHNIQUES 8. WEAVER'S VILLAGES");
	}
	static void routepocham()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Metro");

		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Bbus();
			else
				routepocham();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				mmetro();
			else
				routepocham();
			break;
		default:

			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				routepocham();  
		}
	}
	static void Bbus()
	{
		System.out.println("POCHAMPALLY TO VIKARABAD AVALIBLE TRAIN NO:1.57687,2.(TSRTC)");    
	}
	static void  mmetro()
	{
		System.out.println("POCHAMPALLY TO CHILKUR BALAJI AVALIBLE METRO NO:1.57687,2.(TSRTC)");    
	}
	static void Bhadhrachalam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Bhadhrachalam");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");        
		int An= sc.nextInt();
		switch(An)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				plaace();
			else
				Bhadhrachalam();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				famoufood();
			else
				Bhadhrachalam();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))
				routebhad();
			else
				Bhadhrachalam();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				Bhadhrachalam();

		}
	}
	static void plaace()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Bhadrachalam");
		System.out.println(blue+def+space2+"\t\t\t1.Bhadrachalam Temple" +"\n"+space2+ "\t\t\t2.Parnasala" +"\n"+space2+"\t\t\t3.Siri Rama Giri"+"\n"+space2+"\t\t\t4.Papi Hills");          
	}

	static void famoufood()
	{
		System.out.println("Famous  food : 1.prasadam 2.SWEETS 3.PULIHORA 4.andhra cuisions 5.cultural handcrafts 6. sabari river 7. TYDA PARK 8. spirtual ertral 9.rasam ");

	}
	static void routebhad()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Merto");		
		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES")) 
				bbuus();
			else
				routebhad();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				mmetroo();
			else
				routebhad();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				routebhad();   
		}
	}
	static void bbuus()
	{
		System.out.println("BHADHRACHALAM TO CHILKUR BALAJI AVALIBLE BUS NO:1.57687,2.(TSRTC)");    
	}
	static void  mmetroo()
	{
		System.out.println("BHADHRACHALAM TO VIKARABAD AVALIBLE METRO NO:1.57687,2.(TSRTC)");    
	}
	static void tour_package()
	{

	}
	static void hyderabad()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\tYou have Selected  Hyderabad");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int An= sc.nextInt();
		switch(An)
		{
		case 1: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				nearplacesss();
			else
				hyderabad();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				ffamoussfood();
			else
				hyderabad();
			break;
		case 3: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))  
				routee();
			else
				hyderabad();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				hyderabad(); 

		}
	}
	static void  nearplacesss()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Hyderabad");
		System.out.println(blue+def+space2+"\t\t\t1.Charminar" +"\n"+space2+ "\t\t\t2.Golconda Fort" +"\n"+space2+"\t\t\t3.Salar Jung Museum"+"\n"+space2+"\t\t\t4.Ramoji Film City"+"\n"+space2+"\t\t\t5.Nagarjuna Sagar");
	}
	static void ffamoussfood()
	{
		System.out.println("Famous food  : 1.CHAI 2.SWEETS 3.PULIHORA 4.ANATHAGIRI TEMPLE 5.SCENIC BEAUTY 6. BONICAL GRADENS 7. MECCA MASJID 8. FALAKNAMA PALACE 9.BANGLES 10. NIZAMS SILVER JUBILEE MUSEUM");

	}
	static void routee()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t      How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");

		//String way = sc.nextInt();
		int fam = sc.nextInt();
		switch(fam)
		{
		case 1: 
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				buuses();
			else
				routee();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				traiin();
			else
				routee();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				routee(); 
		}
	}
	static void buuses()
	{
		System.out.println("HYDERABAD TO CHARMINAR  AVALIBLE BUS NO : 288S, 288R (JBS),(MGBS)");
		System.out.println("HYDERABAD  TO GOLCONDA FORT  AVALIBLE BUS NO: 288S ,(JBS),(MGBS)");
		System.out.println("HYDERABAD  TO SALAR HUNG MUSEUM AVALIBLE BUS NO:288S,( Parli Vaijnath Passenger)");
		System.out.println("HYDERABAD TO RAMOJI FILM CITY  AVALIBLE BUS NO : 288S, 288R (JBS),(MGBS)");
		System.out.println("HYDERABAD TO NARJUNA SAGAR  AVALIBLE BUS NO : 288S, 288R (JBS),(MGBS)");
	}
	static  void traiin()
	{  
		System.out.println("HYDERABAD  TO SALAR JUNG MUSEUM AVALIBLE TRAIN NO:1.57687,2.(TSRTC)");  
		System.out.println("HYDERABAD TO  GOLCONDA AVALIBLE BUS NO :1. 288S,2. 288R 3.(JBS),4.(MGBS)");  
	}


	static void kerala()  
	{
		System.out.println(Bold+green+"------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("\t\t\t\t\t\t\t           *WELCOME TO Kerala*");  
		System.out.println("-----------------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(darkBlue+"kerala, a state on India's tropical Malabar Coast, has nearly 600km of Arabian Sea shoreline. It's known for its palm-lined beaches and backwaters, a network of canals. Inland are the Western Ghats, mountains whose slopes support tea, coffee and spice plantations as well as wildlife. National parks like Eravikulam and Periyar, plus Wayanad and other sanctuaries, are home to elephants, langur monkeys and tigers "+"\n");
		System.out.println(yellow+welcome+"\t      The best time to visit Kerala is from November to February");
		System.out.println(welcome2+def+"\t\t\t\tSelect your dream place to visit");
		System.out.println(space2+"\t\t\t1.KOCHI" +"\n"+ space2+"\t\t\t2.ALAPPUZHA"+"\n"+ space2+"\t\t\t3.MUNNAR" +"\n"+ space2+"\t\t\t4.KOVALAM ");  
		int place=sc.nextInt();
		switch(place)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			KOCHI();
		else
			kerala();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			ALAPPUZHA();
		else
			kerala();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			MUNNAR();
		else
			kerala();
		break;
		case 4:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home3=sc.next();
		if(home3.equals("yes")||home3.equals("YES"))
			KOVALAM();
		else
			kerala();
		break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				kerala();

		}
	}  
	static void KOCHI()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected KOCHI");
		System.out.println(def+space2+" \tPlease make a selection from the below options");
		System.out.println(space2+"\t\t\t1. Near by places" +"\n"+ space2+"\t\t\t2. Famous for " +"\n"+ space2+"\t\t\t3. How to reach");
		int list=sc.nextInt();
		switch(list)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_KOCHI();
		else
			KOCHI();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_KOCHI();
		else
			KOCHI();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_KOCHI();
		else
			KOCHI();
		break;
		default: 
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				KOCHI();
		}
	}
	static void nearby_KOCHI()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near KOCHI");
		System.out.println(blue+def+space2+"\t\t\t1.Lulu International Mall" +"\n"+space2+ "\t\t\t2.Hill Palace Museum" +"\n"+space2+"\t\t\t3.Ernakulam Shiva Temple"+"\n"+space2+"\t\t\t4.Bolgatty Palace and Island");
	}
	static void famous_KOCHI()
	{
		System.out.println(welcome1+"Famous Food :1.Nadan Kozhi Varuthathu 2.Prawn Curry 3.Fish Molee");

	}
	static void route_KOCHI()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t          How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");
		int famous1=sc.nextInt();
		switch(famous1)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus11();
			else
				route_KOCHI();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				train11();
			else
				route_KOCHI();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_KOCHI();

		}
	}
	static void bus11()
	{
		System.out.println(space2+" Kochi Available Buses: 1.224 2.929 3.98D 4.480 5.76E");
	}
	static void train11()
	{
		System.out.println(space2+"kochi : 1.56362 2.74654 3.87654 ");
	}
	static void ALAPPUZHA()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Alappuzha");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+ "\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list1=sc.nextInt();
		switch(list1)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_ALAPPUZHA();
		else
			ALAPPUZHA();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_ALAPPUZHA();
		else
			ALAPPUZHA();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_ALAPPUZHA();
		else
			ALAPPUZHA();
		break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				ALAPPUZHA();
		}
	}
	static void nearby_ALAPPUZHA()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near ALAPPUZHA");
		System.out.println(blue+def+space2+"\t\t\t1.INTERNATIONAL COIR MUSEUM"+"\n"+space2+"\t\t\t2.Oscar Cruise"+"\n"+space2+"\t\t\t3.Alappuzha Light House"+"\n"+space2+"\t\t\t4.Alappuzha Beach");

	}
	static void famous_ALAPPUZHA()
	{
		System.out.println(welcome+"Famous Food : 1.Dosa 2.Sambar vada 3.karimeen curry");


	}
	static void route_ALAPPUZHA()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");
		int famous2=sc.nextInt();
		switch(famous2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus21();
			else
				route_ALAPPUZHA();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				train21();
			else
				route_ALAPPUZHA();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_ALAPPUZHA();

		}                   
	}
	static void bus21()
	{
		System.out.println(space2+"ALAPPUZHA Available Buses: 1.224 2.929 3.98D 4.480 5.76E");
	}
	static void train21()
	{
		System.out.println(space2+"ALAPPUZHA : 1. 85647  2.98764  3.09865  4.17548 ");
	}
	static void MUNNAR()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected MUNNAR");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_MUNNAR();
		else
			MUNNAR();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_MUNNAR();
		else
			MUNNAR();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_MUNNAR();
		else
			MUNNAR();
		break;
		default :
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				MUNNAR();
		}
	}
	static void nearby_MUNNAR()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near MUNNAR");
		System.out.println(blue+def+space2+"\t\t\t1.Munnar Hiking Trails"+"\n"+space2+"\t\t\t2.Top Station"+"\n"+space2+"\t\t\t3.Eravikulam National Park"+"\n"+space2+"\t\t\t4.Hydel Park parking ground");

	}
	static void famous_MUNNAR()
	{
		System.out.println(welcome1+"Famous Food : 1.Ari Pathri and Chicken Curry 2.Appam and prawn curry 3.Idiyappam with Egg Curry");


	}
	static void route_MUNNAR()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t          How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");
		int famous3=sc.nextInt();
		switch(famous3)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus33();
			else
				route_MUNNAR();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cabs33();
			else
				route_MUNNAR();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_MUNNAR();

		}                     
	}
	static void bus33()
	{
		System.out.println(space2+"Munnar Available Buses: 1.24E 2.99D 3.98D 4.48W 5.76E");
	}
	static void cabs33()
	{
		System.out.println(space2+"MUNNAR Available Trains: 1. 67464  2.36363 3.65443  4. 56749 ");
	}
	static void KOVALAM()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected  KOVALAM");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_KOVALAM();
		else
			KOVALAM();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_KOVALAM();
		else
			KOVALAM();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_KOVALAM();
		else
			KOVALAM();
		break;
		default :
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				KOVALAM();
		}
	}
	static void nearby_KOVALAM()
	{

		System.out.println(Bold+blue+space2+"\t         Places to Visit Near  KOVALAM");
		System.out.println(blue+def+space2+"\t\t\t1.Rockholm at the Light House Beach"+"\n"+space2+"\t\t\t2.Kovalam Beach"+"\n"+space2+"\t\t\t3.Bond Safari Scuba Diving "+"\n"+space2+"\t\t\t4.Sree Padmanabhaswamy Temple");
	}
	static void famous_KOVALAM()
	{
		System.out.println(welcome+"Famous Food : 1.Crabs and lobsters 2.Kappa 3.Puttu");


	}
	static void route_KOVALAM()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");
		int famous4=sc.nextInt();
		switch(famous4)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus44();
			else
				route_KOVALAM();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				train44();
			else
				route_KOVALAM();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_KOVALAM();

		}                     

	}
	static void bus44()
	{
		System.out.println(welcome+"KOVALAM Available Buses: 1.224 2.929 3.98D 4.480 5.76E");
	}
	static void train44()
	{
		System.out.println(welcome1+"KOVALAM : 1.35467  2. 33454  3.46754  4.98765 ");
	}
	static void andhrapradesh()
	{

	}
	static void north()  
	{
		System.out.println(Bold+skblue+"-----------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(Bold+skblue+blink+"\t\t\t\t\t\t\t\t**WELCOME TO NORTH INDIA**");   
		System.out.println(    "------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(def+"\t\t\t\t\t\t\t    Choose one state from the following");
		System.out.println("\t\t\t\t\t\t\t    1.uttarakhand 2.J&K 3.Delhi");   
		int state=sc.nextInt();
		switch(state)
		{   
		case 1:
			System.out.print("Do you want to continue with North , if yes enter yes else no: ");
			String home=sc.next();
			if(home .equals ("yes"))
				uttarakhand();
			else
				north();

			break; 
		case 2:System.out.print("Do you want to continue with North , if yes enter yes else no: ");
		String home1=sc.next();
		if(home1.equals ("yes"))
			J_K();
		else
			north();

		break; 
		case 3:
			System.out.print("Do you want to continue with North , if yes enter yes else no: ");
			String home2=sc.next();
			if(home2.equals ("yes"))
				delhi();
			else
				north();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				north();

		}  
	}
	static void uttarakhand()  
	{
		System.out.println(Bold+green+"------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("\t\t\t\t\t\t\t        *WELCOME TO UTTARAKHAND*");  
		System.out.println("---------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(darkBlue+"Uttarakhand, often referred to as the Devbhoomi or Land of the Gods,  is a northern Indian state nestled in the Himalayas. Its a region of    great spiritual significance with numerous ancient temples and pilmgimage sites, attracting devotees and seekers of inner peace. Uttarakhand's diverse landscapes offer oppurtunities for adventure enthusiasists, from trekking in the majestoc Himalayan ranges to white water rafting in its sacred rivers."+"\n");
		System.out.println(yellow+welcome+"\t      The best time to visit Uttarakhand is from March to April and September to October");
		System.out.println(welcome2+def+"\t\t\t\tSelect your dream place to visit");
		System.out.println(space2+"\t\t\t1.Haridwar" +"\n"+ space2+"\t\t\t2.Rishikesh "+"\n"+ space2+"\t\t\t3.Mussorie" +"\n"+ space2+"\t\t\t4.Dehradun " +"\n"+space2+"\t\t\t5.Kedarnath & Badrinath");  
		int place=sc.nextInt();
		switch(place)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Haridwar();
			else
				uttarakhand();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				Rishikesh();
			else
				uttarakhand();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				Mussorie();
			else
				uttarakhand();
			break;
		case 4:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))
				Dehradun();
			else
				uttarakhand();
			break;
		case 5:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home4=sc.next();
			if(home4.equals("yes")||home4.equals("YES"))
				Kedarnath();
			else
				uttarakhand();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			uttarakhand();

		}
	}  
	static void Haridwar()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Haridwar");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list=sc.nextInt();
		switch(list)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_Hari();
			else
				Haridwar();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_Hari();
			else
				Haridwar();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_Hari();
			else
				Haridwar();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Haridwar();
		}
	}
	static void nearby_Hari()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Haridwar");
		System.out.println(space2+def+"\t\t\t1.Har Ki Pauri "+"\n"+space2+"\t\t\t2.Manasa Devi Temple "+"\n"+space2+"\t\t\t3.Chandi Devi Temple "+"\n"+space2+"\t\t\t4.Kankhal"+"\n");  


	}
	static void famous_Hari()
	{
		System.out.println("Famous Food : 1.Aloo puri 2.Chole Bhature 3.Rabri 4.Jalebi");
		System.out.println("Famous Things : 1.Ganga Aarti 2.Ganga Jal 3.Rudraksha Beads 4.Spiritual Books");

	}
	static void route_Hari()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Bush();
			else
				route_Hari();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				Cabh();
			else
				route_Hari();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			route_Hari();
		}
	}
	static void Bush()
	{
		System.out.println("Available for Haridwar: 1.235 2.569 3.458 4.85");
	}
	static void Cabh()
	{
		System.out.println("Cabs are available for Haridwar");
	}
	static void Rishikesh()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Rishikesh");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list1=sc.nextInt();
		switch(list1)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_Rishi();
			else
				Rishikesh();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_Rishi();
			else
				Rishikesh();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_Rishi();
			else
				Rishikesh();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Rishikesh();
		}
	}
	static void nearby_Rishi()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Rishikesh");
		System.out.println(blue+def+space2+"\t\t\t1. Laxman Jhula and Ram Jhula"+"\n"+space2+"\t\t\t2. Triveni Ghat "+"\n"+space2+"\t\t\t3. Neelkanth Mahadev Temple"+"\n"+space2+"\t\t\t4. Parmarth Niketan Ashram"+"\n");  

	}
	static void famous_Rishi()
	{
		System.out.println("Famous Food : 1.Pakoras 2.Rajma Chawal 3.Thukpa 4.parathas");
		System.out.println("Famous Things : 1.Yoga & Meditation Accessories 2.Handicrafts 3.Musical Instruments 4.Gemstones and Crystals");

	}
	static void route_Rishi()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Busr();
			else
				route_Rishi();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				Cabr();
			else
				route_Rishi();
			break;  
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			route_Rishi(); 
		}                    
	}
	static void Busr()
	{
		System.out.println("Available for Rishikesh : 1.23 2.56 3.63 4.97");
	}
	static void Cabr()
	{
		System.out.println("Cabs are available for Rishikesh");
	}
	static void Mussorie()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Mussorie");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_Mus();
			else
				Mussorie();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_Mus();
			else
				Mussorie();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_Mus();
			else
				Mussorie();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Mussorie();
		}
	}
	static void nearby_Mus()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Mussorie");
		System.out.println(def+space2+"\t\t\t1. Kempty Falls "+"\n"+space2+"\t\t\t2. Gun Hill "+"\n"+space2+"\t\t\t3. Camels Back Road "+"\n"+space2+"\t\t\t4. Mall Road "+"\n");  

	}
	static void famous_Mus()
	{
		System.out.println("Famous Food : 1.Bun Omlette 2.Chowmein 3.Pahadi Cuisine 4.Mutton Curry");
		System.out.println("Famous Things : 1.Woolens and Shawls 2.Local Jewwelry 3.Handmade Soaps & candles 4.Wine and Local Procure");

	}
	static void route_Mus()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Busm();
			else
				route_Mus();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				Cabm();
			else
				route_Mus();
			break;  
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			route_Mus();
		}                      
	}
	static void Busm()
	{
		System.out.println("Available for Mussorie : 1.256 2.089 3.076 4.198");
	}
	static void Cabm()
	{ 
		System.out.println("Cabs are available for Mussorie");
	}
	static void Dehradun()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Dehradun");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_Deh();
			else
				Dehradun();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_Deh();
			else
				Dehradun();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_Deh();
			else
				Dehradun();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Dehradun();
		}
	}
	static void nearby_Deh()
	{

		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Dehradun");
		System.out.println(def+space2+"\t\t\t1.Robbers Cave"+"\n"+space2+"\t\t\t2.Sahastradhara"+"\n"+space2+"\t\t\t3.Tapkeshwar Temple"+"\n"+space2+"\t\t\t4.Forest Research Institute");
	}
	static void famous_Deh()
	{
		System.out.println("Famous Food : 1.Aloo Ke Gutke 2.Garma Garam Jalebi 3.Lassi 4.Kanchori Sabzi");
		System.out.println("Famous Things : 1.Flavoured Honey 2.Himalayan Herbal Products 3.Uttarakhand Tea 4.Wooden Handicrafts");

	}
	static void route_Deh()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Busd();
			else
				route_Deh();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				Cabd();
			else
				route_Deh();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			route_Deh();
		}
	}
	static void Busd()
	{
		System.out.println("Available for Denradun : 1.552 2.366 3.91 4.23");
	}
	static void Cabd()
	{
		System.out.println("Cabs are available for Dehradun");
	}
	static void Kedarnath()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Kedarnath & Badrinath");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list=sc.nextInt();
		switch(list)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_Ked();
			else
				Kedarnath();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_Ked();
			else
				Kedarnath();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back: ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_Ked();
			else
				Kedarnath();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Kedarnath();
		}
	}
	static void nearby_Ked()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Kedarnath & Badrinath");
		System.out.println(def+space2+"\t\t\t1. Badrinath Temple"+"\n"+space2+"\t\t\t2. Vasuki Tal "+"\n"+space2+"\t\t\t3. Kedarnath Temple"+"\n"+space2+"\t\t\t4. Auli"+"\n");  

	}
	static void famous_Ked()
	{
		System.out.println("Famous Food : 1.Simple North Indian Meal 2.Puri Sabzi 3.North Indian Thali 4.Prasad");
		System.out.println("Famous Things : 1.Small Idols 2.Spices and Herbs 3.Copper and Brass Utensils 4.Chandan");

	}
	static void route_Ked()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int fam=sc.nextInt();
		switch(fam)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				Busk();
			else
				route_Ked();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				Cabk();
			else
				route_Ked();
			break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			route_Ked();
		}

	}
	static void Busk()
	{
		System.out.println("Available for Kedarnath : 1.325 2.486 3.124 4.032");
	}
	static void Cabk()
	{
		System.out.println("kedarnath : Cabs are availabe");
	}


	static void J_K()
	{
		System.out.println(Bold+green+"----------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("\t\t\t\t\t\t\t        WELCOME TO JAMMU AND KASHMIR");  
		System.out.println(           "----------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(darkBlue+"Jammu and Kashmir is a region administered by India as a union territory and consists of the southern portion of the larger Kashmir region, which has been the subject of a dispute between India and Pakistan since 1947 and between India and China since 1959"+"\n");
		System.out.println(yellow+welcome+"\t           The best time to visit JAMMU AND KASHMIR is from DECEMBER to March");
		System.out.println(welcome2+def+"\t\t\t\tSelect your dream place to visit");
		System.out.println(space2+"\t\t\t1.PAHALGAM"+"\n"+space2+"\t\t\t2.KASHMIR"+"\n"+space2+"\t\t\t3.SRINAGAR"+"\n"+space2+"\t\t\t4.LADAKH");
		int place=sc.nextInt();
		switch(place)
		{
		case 1: System.out.print("Type YES for continue OR type NO to go back: ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			Pahalgam();
		else
			J_K();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back: ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			Kashmir();
		else
			J_K();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back: ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			Srinagar();
		else
			J_K();
		break;
		case 4:System.out.print("Type YES for continue OR type NO to go back: ");
		String home3=sc.next();
		if(home3.equals("yes")||home3.equals("YES"))
			Ladakh();
		else
			J_K();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			J_K();

		}
	}  
	static void Pahalgam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Pahalgam");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list=sc.nextInt();
		switch(list)
		{
		case 1: System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Pahalgam();
		else
			Pahalgam();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Pahalgam();
		else
			Pahalgam();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Pahalgam();
		else
			Pahalgam();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the region enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Pahalgam();
		}
	}
	static void nearby_Pahalgam()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Pahalgam");
		System.out.println(space2+def+"\t\t\t1.AMARNATH" +"\n"+ space2+"\t\t\t2.ARU VALLEY" +"\n"+ space2+"\t\t\t3.KOHALOI GLACIER" +"\n"+ space2+"\t\t\t4.BETAAB VALLEY");

	}
	static void famous_Pahalgam()
	{
		System.out.println(space2+"Famous Food :"+"\n"+space2+"1.Matscspace"+"\n"+space2+"hgand"+"\n"+space2+"2.kaanti"+"\n"+space2+"3.Aab Gosht");

	}
	static void route_Pahalgam()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");	    
		int famousl=sc.nextInt();
		switch(famousl)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				busl();
			else
				route_Pahalgam();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cabl();
			else
				route_Pahalgam();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Pahalgam();

		}
	}
	static void busl()
	{
		System.out.println("pahalgam Available Buses: 1.324 2.329 3.43E 4.480 5.54F");
	}
	static void cabl()
	{
		System.out.println("pahalgam : cabs available ");
	}


	static void Kashmir()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Kashmir");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list1=sc.nextInt();
		switch(list1)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Kashmir();
		else
			Kashmir();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Kashmir();
		else
			Kashmir();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Kashmir();
		else
			Kashmir();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Kashmir();
		}
	}
	static void nearby_Kashmir()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Kashmir");
		System.out.println(def+space2+"\t\t\t1.SONMARG"+"\n"+space2+"\t\t\t2.GULMARG"+"\n"+space2+"\t\t\t3.PATNITOP"+"\n"+space2+"\t\t\t4.SANASAR");

	}
	static void famous_Kashmir()
	{
		System.out.println(space2+"Famous Food :"+"\n"+space2+"1.Paneer Chaman"+"\n"+space2+"3.Kashmir Saag"+"\n"+space2+"2.Dum Olav");

	}
	static void route_Kashmir()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int famous2=sc.nextInt();
		switch(famous2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus2();
			else
				route_Kashmir();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab2();
			else
				route_Kashmir();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Kashmir();

		}
	}
	static void bus2()
	{
		System.out.println("pahalgam Available Buses: 1.244 2.149 3.345 4.480 5.143");
	}
	static void cab2()
	{
		System.out.println("pahalgam : cabs available ");
	}
	static void Srinagar()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Srinagar");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		

		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back, ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_Srinagar();
			else
				Srinagar();
			break;
		case 2:System.out.print("Type YES for continue OR type NO to go back, ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Srinagar();
		else
			Srinagar();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back, ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Srinagar();
		else
			Srinagar();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Srinagar();
		}
	}
	static void nearby_Srinagar()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Srinagar");
		System.out.println(def+space2+"\t\t\t1.KOKERNAG"+"\n"+space2+"\t\t\t2.Doodh pathri"+"\n"+space2+"\t\t\t3.fotula"+"\n"+space2+"\t\t\t4.sinadh top");

	}
	static void famous_Srinagar()
	{
		System.out.println(space2+"Famous Food :"+"\n"+space2+"1.Seekh kebabs"+"\n"+space2+"2.Wazman Saag"+"\n"+space2+"3.KEsar Phirni");

	}
	static void route_Srinagar()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int famous3=sc.nextInt();
		switch(famous3)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus3();
			else
				route_Srinagar();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab3();
			else
				route_Srinagar();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Srinagar();

		}
	}
	static void bus3()
	{
		System.out.println("pahalgam Available Buses: 1.124 2.129 3.33E 4.4970 5.532F");
	}
	static void cab3()
	{
		System.out.println("pahalgam : cabs available ");
	}
	static void Ladakh()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Ladakh");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		

		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home=sc.next();
		if(home.equals("yes")||home.equals("YES"))
			nearby_Ladakh();
		else
			Ladakh();
		break;
		case 2:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home1=sc.next();
		if(home1.equals("yes")||home1.equals("YES"))
			famous_Ladakh();
		else
			Ladakh();
		break;
		case 3:System.out.print("Type YES for continue OR type NO to go back :  ");
		String home2=sc.next();
		if(home2.equals("yes")||home2.equals("YES"))
			route_Ladakh();
		else
			Ladakh();
		break;
		default:System.out.println(red+"You Have Entered Invalid Number"+def);
		System.out.println("If You want to go back to the place enter back");
		String back=sc.next().toLowerCase();
		if(back==back)
			Ladakh();
		}
	}
	static void nearby_Ladakh()
	{

		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Ladakh");
		System.out.println(def+space2+"\t\t\t1.LEH"+"\n"+space2+"\t\t\t2.Zanskar"+"\n"+space2+"\t\t\t3.nubra valleys"+"\n"+space2+"\t\t\t4.Kargil");
	}
	static void famous_Ladakh()
	{
		System.out.println(space2+"Famous Food :"+"\n"+space2+"1.Tingmo"+"\n"+space2+"2.Chhupre"+"\n"+space2+"3.Butter tea");

	}
	static void route_Ladakh()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Cab");		
		int famous4=sc.nextInt();
		switch(famous4)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				bus4();
			else
				route_Ladakh();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				cab4();
			else
				route_Ladakh();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_Ladakh();

		}
	}
	static void bus4()
	{
		System.out.println("pahalgam Available Buses: 1.224 2.929 3.98D 4.480 5.76E");
	}
	static void cab4()
	{
		System.out.println("pahalgam : cabs available ");
	}
	static void delhi()  
	{
		System.out.println(Bold+green+"------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println("\t\t\t\t\t\t\t            *WELCOME TO DELHI*");  
		System.out.println(   "------------------------------------------------------------------------------------------------------------------------------------------------------------");
		System.out.println(darkBlue+"       Delhi, India’s capital territory, is a massive metropolitan area in the country’s north. In Old Delhi, a neighborhood dating to the 1600s, stands the imposing Mughal-era Red Fort, a symbol of India, and the sprawling Jama Masjid mosque, whose courtyard accommodates 25,000 people"+"\n");
		System.out.println(yellow+welcome+"\t           The best time to visit Delhi is from October to March");
		System.out.println(welcome2+def+"\t\t\t\tSelect your dream place to visit");
		System.out.println(space2+"\t\t\t1.Lotus Temple" +"\n"+ space2+"\t\t\t2.India Gate "+"\n"+ space2+"\t\t\t3.Red Fort" +"\n"+ space2+"\t\t\t4.Qutub Minar " +"\n"+space2+"\t\t\t5.Swaminarayan Akshardham");  
		int place=sc.nextInt();
		switch(place)
		{
		case 1: 
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				lotus_temple();
			else
				delhi();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				india_gate();
			else
				delhi();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_gate();
			else
				delhi();
			break;
		case 4:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home3=sc.next();
			if(home3.equals("yes")||home3.equals("YES"))
				qutub_minar();
			else
				delhi();
			break;
		case 5:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home4=sc.next();
			if(home4.equals("yes")||home4.equals("YES"))
				swaminarayan_akshardham();
			else
				delhi();
			break;

		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				delhi();

		}
	}  
	static void lotus_temple()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Lotus Temple");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list=sc.nextInt();
		switch(list)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_lotus();
			else
				lotus_temple();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_lotus();
			else
				lotus_temple();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_lotus();
			else
				lotus_temple();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				lotus_temple();

		}
	}
	static void nearby_lotus()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Lotus Temple");
		System.out.println(def+space2+"\t\t\t1.Delhi Haat" +"\n"+ space2+"\t\t\t2.ISKCON Temple" +"\n"+ space2+"\t\t\t3.Go City Adventures" +"\n"+ space2+"\t\t\t4.The Lost Compass" +"\n"+ space2+"\t\t\t5.Nehru Place");

	}
	static void famous_lotus()
	{
		System.out.println(welcome1+"     Famous Food : 1.Pakodas 2.Jalebu 3.Lassi");

	}
	static void route_lotus()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");	    

		int famousl=sc.nextInt();
		switch(famousl)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				busL();
			else
				route_lotus();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				trainL();
			else
				route_lotus();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_lotus();

		}
	}
	static void busL()
	{
		System.out.println("Delhi to Lotus Temple Available Buses: 1.424 2.429 3.433 4.480 5.534");
	}
	static void trainL()
	{
		System.out.println("Delhi to Lotus Temple Available Trains: 1.EMU 64012 2.EMU 64078");
	}

	static void india_gate()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected India Gate");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list1=sc.nextInt();
		switch(list1)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_gate();
			else
				india_gate();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_gate();
			else
				india_gate();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_gat();
			else
				india_gate();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				india_gate();

		}
	}
	static void nearby_gate()
	{
		System.out.println(Bold+blue+space2+"\t          Places to Visit Near India Gate");
		System.out.println(space2+def+"\t\t\t1.Delhi Photo Tour" +"\n"+ space2+"\t\t\t2.Delhi With Loki" +"\n"+ space2+"\t\t\t3.National War Memorial" +"\n"+ space2+"\t\t\t4.Pradhanmantri Sangrahalaya" +"\n"+ space2+"\t\t\t5.Rajpath");

	}
	static void famous_gate()
	{
		System.out.println(welcome1+"     Famous Food : 1.Chaat 2.Parathas 3.Street Sweets");

	}
	static void route_gat()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");			
		int famousg=sc.nextInt();
		switch(famousg)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				busg();
			else
				route_gate();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				traing();
			else
				route_gate();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_gate();

		}
	}
	static void busg()
	{
		System.out.println("Delhi to IndiaGate Available Buses: 1.181A 2.181B 3.451A 4.456 5.502");
	}
	static void traing()
	{
		System.out.println("Delhi to IndiaGate Available Trains: 1.EMU 64090 2.EMU 64091");
	}
	static void route_gate()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Red Fort");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_redfort();
			else
				route_gate();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_redfort();
			else
				route_gate();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_redfort();
			else
				route_gate();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_gate();

		}
	}
	static void nearby_redfort()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Red Fort");
		System.out.println(space2+def+"\t\t\t1.Gurudwara Sri Bangla Sahib" +"\n"+ space2+"\t\t\t2.Humayun’s Tomb" +"\n"+ space2+"\t\t\t3.Lodhi Garden" +"\n"+ space2+"\t\t\t4.Chandni Chowk");

	}
	static void famous_redfort()
	{
		System.out.println(welcome1+"     Famous Food : 1.Churros 2.Thali At Grover Eating Point 3.Jalebi");

	}
	static void route_redfort()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");		   
		int famousr=sc.nextInt();
		switch(famousr)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				busr();
			else  
				route_redfort();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				trainr();
			else  
				route_redfort();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_redfort();

		}
	}
	static void busr()
	{
		System.out.println("Delhi to Redfort Temple Available Buses: 1.120B 2.185 3.214CL 4.347 5.425");
	}
	static void trainr()
	{
		System.out.println("Delhi to Redfort Temple Available Trains: 1.EMU 64091 2.EMU 64439");
	}
	static void qutub_minar()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Qutub Minar");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		
		int list2=sc.nextInt();
		switch(list2)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_qutub();
			else
				qutub_minar();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_qutub();
			else
				qutub_minar();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_qutub();
			else
				qutub_minar();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				qutub_minar();
		}
	}
	static void nearby_qutub()
	{

		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Qutub Minar");
		System.out.println(space2+def+"\t\t\t1.Tomb of Imam Zamin" +"\n"+ space2+"\t\t\t2.Quwwat-ul-Islam Mosque" +"\n"+ space2+"\t\t\t3.Iron Pillar of Delhi" +"\n"+ space2+"\t\t\t4.ltutmish's Tomb" +"\n"+ space2+"\t\t\t5.Smith's Folly");
	}
	static void famous_qutub()
	{
		System.out.println("Famous Food : 1.Butter Chicken 2.Coffee and Chai 3.Mutton Galouti kebabs");

	}
	static void route_qutub()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");			
		int famousq=sc.nextInt();
		switch(famousq)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				busq();
			else
				route_qutub();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				trainq();
			else
				route_qutub();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_qutub();

		}
	}
	static void busq()
	{
		System.out.println("Delhi to QutubMinar Available Buses: 1.400 2.433CL 3.460 4.460CL 5.512");
	}
	static void trainq()
	{
		System.out.println("Delhi to QutubMinar Available Trains: 1.EMU 64090 2.EMU 64094");
	}
	static void swaminarayan_akshardham()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t    You have Selected Swaminarayan Akshardham");
		System.out.println(def+space2+" \tPlease make a selection from the below options:");
		System.out.println(space2+"\t\t\t1. Near by places"+"\n"+space2+"\t\t\t2. Famous for"+"\n"+space2+ "\t\t\t3. How to reach");		

		int list=sc.nextInt();
		switch(list)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				nearby_swaminarayan_Akshardham();
			else
				swaminarayan_akshardham();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				famous_swaminarayan_Akshardham();
			else
				swaminarayan_akshardham();
			break;
		case 3:
			System.out.print("Type YES for continue OR type NO to go back");
			String home2=sc.next();
			if(home2.equals("yes")||home2.equals("YES"))
				route_swaminarayan_Akshardham();
			else
				swaminarayan_akshardham();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				swaminarayan_akshardham();


		}
	}
	static void nearby_swaminarayan_Akshardham()
	{
		System.out.println(Bold+blue+space2+"\t         Places to Visit Near Swaminarayan Akshardham");
		System.out.println(space2+def+"\t\t\t1.Taj Mahal" +"\n"+ space2+"\t\t\t2.Sunder Nursery Park" +"\n"+ space2+"\t\t\t3.Masterji Ki Haveli" +"\n"+ space2+"\t\t\t4.Humayun's thomb");

	}
	static void famous_swaminarayan_Akshardham()
	{
		System.out.println(welcome1+"     Famous Food : 1.Mithai 2.Local Beverages 3.Fast Food 4.Street Snacks");
		System.out.println(welcome1+"     Famous Things : 1.Cultural Performance 2.Light and Sound Show");

	}
	static void route_swaminarayan_Akshardham()
	{
		System.out.println(Bold+blue+welcome1+"\t\t\t\t         How to reach");
		System.out.println(welcome2+def+"\t\t\t\tselect transport 1.Bus 2.Train");			
		int famouss=sc.nextInt();
		switch(famouss)
		{
		case 1:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home=sc.next();
			if(home.equals("yes")||home.equals("YES"))
				buss();
			else
				route_swaminarayan_Akshardham();
			break;
		case 2:
			System.out.print("Type YES for continue OR type NO to go back :  ");
			String home1=sc.next();
			if(home1.equals("yes")||home1.equals("YES"))
				trains();
			else
				route_swaminarayan_Akshardham();
			break;
		default:
			System.out.println(red+"You Have Entered Invalid Number"+def);
			System.out.println("If You want to go back to the region enter back");
			String back=sc.next().toLowerCase();
			if(back==back)
				route_swaminarayan_Akshardham();

		}
	}
	static void buss()
	{
		System.out.println("Delhi to Swaminarayan Akshardham Available Buses: 1.357 2.473EXTN 3.661B");
	}
	static void trains()
	{
		System.out.println("Delhi to Swaminarayan Akshardham Available Trains: 1.EMU 64031 2.EMU 64055 ");
	}
	static int n;
	static double totalCost;
	static void pack()
	{
		Scanner scanner = new Scanner(System.in);
		System.out.println();
		System.out.println(Bold+green+welcome+"\t      Base Package Price for 1 person is: RS " + TripPackage.BASE_PRICE);
		System.out.println(Bold+green+welcome+"\t      0.9% Discount is applied for 10 or more than 10 people"+"\n");
		System.out.print(def+space2+"\t     Enter the package name: ");
		String packageName = scanner.nextLine();

		TripPackage package1 = new TripPackage(packageName);

		System.out.println(space2+"\t     Enter the number of people: ");
		n = scanner.nextInt();

		totalCost = package1.calculateTotalCost(n);

		System.out.println(space2+"\t     Package: " + package1.getPackageName());

		if (n == 1) {
			System.out.println(space2+"\t     Total Amount: RS " +totalCost);
		} else {
			System.out.println(space2+"\t     Total Amount for " + n + " people: RS " + totalCost);
		}
		System.out.println(darkBlue+space2+"\t     Select a payment method:");
		System.out.println(def+space2+"\t     1. Card Payment");
		System.out.println(space2+"\t     2. UPI Payment");
		System.out.print(space2+"\t     Enter your choice: ");
		int choice = scanner.nextInt();
		scanner.nextLine(); // Consume newline

		Payment payment;

		if (choice == 1) {
			System.out.println(blue+space2+"\t     Select a bank:");
			System.out.println(def+space2+"\t     1. SBI");
			System.out.println(space2+"\t     2. HDFC");
			System.out.println(space2+"\t     3. Central Bank");
			System.out.print(blue+space2+"\t     Enter your bank choice: ");
			int bankChoice = scanner.nextInt();
			scanner.nextLine(); // Consume newline

			String bankName;
			if (bankChoice == 1) {
				bankName = "SBI";
			} else if (bankChoice == 2) {
				bankName = "HDFC";
			} else if (bankChoice == 3) {
				bankName = "Central Bank";
			} else {
				System.out.println(red+space2+"\t     Invalid bank choice. Payment failed.");
				return;
			}

			System.out.print(def+space2+"\t     Enter card number: ");
			String cardNumber = scanner.nextLine();
			System.out.print(space2+"\t     Enter card expiry (MM/YY): ");
			String cardExpiry = scanner.nextLine();
			System.out.print(space2+"\t     Enter CVV: ");
			int cvv = scanner.nextInt();
			scanner.nextLine(); // Consume newline

			payment = new Payment("Card Payment");
			payment.makeCardPayment(bankName, cardNumber, cardExpiry, cvv);
		} else if (choice == 2) {
			System.out.print(space2+"\t     Enter UPI ID: ");
			String upiId = scanner.nextLine();

			payment = new Payment("UPI Payment");
			payment.makeUpiPayment(upiId);
		} else {
			System.out.println(red+space2+"\t     Invalid choice. Payment failed.");
			pack();
		}
	}
	public static void main(String args[])
	{  
		ob.sign_log();
		tour();
		System.out.println("\n\n");
		System.out.println(yellow+space2+"\tSelect one for 1 continue......"+" or "+red+" Enter Any key for EXIT");
		int packNum=sc.nextInt();
		switch(packNum)
		{
		case 1:pack();break;
		default :System.out.println(yellow+space2+"\t     THANK FOR REACHING US");
		System.out.println(yellow+space2+"\t     OUR CONTACT DETATILS ");
		System.out.println(yellow+space2+"\t     Email                : wonders@gmail.com");
		System.out.println(yellow+space2+"\t     Mobile	       : 9876543210");
		System.out.println(yellow+space2+"\t     Address              : DOOR NO : 174/5,HYDERABAD, KPHB COLONY,");
		System.out.println(yellow+space2+"\t                            ROAD NUMBER-2, NEAR CV CORP INSTITUE");	
		}

		System.out.println("\n\n");
		System.out.println(green+space3+blink+welcome2+"@@@@@"+"\t"+"@   @"+"\t"+"  @  "+"\t"+"@   @"+"\t"+"@   @");
		System.out.println(welcome2+space3+"  @  "+"\t"+"@   @"+"\t"+" @ @ "+"\t"+"@@  @"+"\t"+"@  @");
		System.out.println(welcome2+space3+"  @  "+"\t"+"@@@@@"+"\t"+"@   @"+"\t"+"@ @ @"+"\t"+"@@@");
		System.out.println(welcome2+space3+"  @  "+"\t"+"@   @"+"\t"+"@@@@@"+"\t"+"@  @@"+"\t"+"@  @");
		System.out.println(welcome2+space3+"  @  "+"\t"+"@   @"+"\t"+"@   @"+"\t"+"@   @"+"\t"+"@   @");
		System.out.println();
		System.out.println(welcome2+space3+"                     "+"@   @"+"                        ");
		System.out.println(welcome2+space3+"                     "+"@   @"+"                        ");
		System.out.println(welcome2+space3+"                     "+"@   @"+"                        ");
		System.out.println(welcome2+space3+"                     "+"@   @"+"                        ");
		System.out.println(welcome2+space3+"                     "+" @@@"+"                         "+def);

	}
}
class TripPackage extends Main
{
	static final double BASE_PRICE = 10000.0; 
	private String packageName;

	public TripPackage(String packageName) 
	{
		this.packageName = packageName;
	}

	public double calculateTotalCost(int n) 
	{
		double totalCost = BASE_PRICE * n;
		if (n >= 10) 
		{
			totalCost *= 0.9;
		}

		return totalCost+50;
	}

	public String getPackageName() 
	{
		return packageName;
	}
	TripPackage(){}

}

class Payment extends TripPackage{
	static String red="\u001B[31m";
	static String green="\u001B[32m";
	static String yellow="\u001B[33m";
	static String space2="                                                ";
	private String paymentMethod;
	private int otp;
	static TripPackage trip=new TripPackage();
	public Payment(String paymentMethod) {
		this.paymentMethod = paymentMethod;
	}

	public int generateRandomOTP() {
		Random random = new Random();
		return random.nextInt(9000) + 1000; // Generate a 4-digit OTP
	}

	public void makeCardPayment(String bankName, String cardNumber, String cardExpiry, int cvv) {
		otp = generateRandomOTP();

		System.out.println("                                           		Payment Method  : " + paymentMethod);
		System.out.println("                                           		Bank            : " + bankName);
		System.out.println("                                           		Card Number     : " + cardNumber);
		System.out.println("                                           		Card Expiry     : " + cardExpiry);
		System.out.println("                                           		CVV		: " + cvv);
		System.out.println("                                   Generated OTP for Card Payment   : " + otp);

		while (true) {
			int enteredOTP = promptForOTP();
			if (enteredOTP == otp) {
				System.out.println("                                           Payment successful!");	
				System.out.println(space2+yellow+"\t    COLLECT YOUR BILL HERE ");
				System.out.println(space2+yellow+"\t    ---------------------------------------------------------------------------");
				System.out.println(space2+yellow+"\t    	YOUR PACAKE  NAME				      :"+getPackageName());
				System.out.println(space2+yellow+"\t    	YOUR TOTAL SQUAD 				      :"+n);
				System.out.println(space2+yellow+"\t    	GST  						      :"+"50");
				System.out.println(space2+yellow+"\t    	TOTAL AMOUNT FOR  "+super.n+" PEOPLE IS               : RS"+totalCost+"\n\n");
				System.out.println(space2+yellow+"\t    	THANK FOR REACHING US");
				System.out.println(space2+yellow+"\t     	OUR CONTACT DETATILS ");
				System.out.println(space2+yellow+"\t    	Email                : wonders@gmail.com");
				System.out.println(space2+yellow+"\t    	Mobile	       	     : 9876543210");
				System.out.println(space2+yellow+"\t     	Address              : DOOR NO : 174/5,HYDERABAD, KPHB COLONY,");
				System.out.println(yellow+space2+"\t                                   ROAD NUMBER-2, NEAR CV CORP INSTITUE");
				System.out.println(space2+yellow+"\t    ---------------------------------------------------------------------------");
				break; // Exit the loop if the OTP is valid
			} else {
				System.out.println("                                           Invalid OTP. Please try again.");
			}
		}
	}

	public void makeUpiPayment(String upiId) {
		otp = generateRandomOTP();

		System.out.println("                                           payment Method: " + paymentMethod);
		System.out.println("                                           UPI ID: " + upiId);
		System.out.println("                                           Generated OTP for UPI Payment: " + otp);

		while (true) {
			int enteredOTP = promptForOTP();
			if (enteredOTP == otp) {
				System.out.println(space2+green+"\t    Payment successful!"+"\n\n");
				System.out.println(space2+yellow+"\t    COLLECT YOUR BILL HERE ");
				System.out.println(space2+yellow+"\t    ---------------------------------------------------------------------------");
				System.out.println(space2+yellow+"\t    	YOUR PACAKE  NAME				      :"+getPackageName());
				System.out.println(space2+yellow+"\t    	YOUR TOTAL SQUAD 				      :"+n);
				System.out.println(space2+yellow+"\t    	GST  						      :"+"50");
				System.out.println(space2+yellow+"\t    	TOTAL AMOUNT FOR  "+super.n+" PEOPLE IS               : RS"+totalCost+"\n\n");
				System.out.println(space2+yellow+"\t    	THANK FOR REACHING US");
				System.out.println(space2+yellow+"\t     	OUR CONTACT DETATILS ");
				System.out.println(space2+yellow+"\t    	Email                : wonders@gmail.com");
				System.out.println(space2+yellow+"\t    	Mobile	       	     : 9876543210");
				System.out.println(space2+yellow+"\t     	Address              : DOOR NO : 174/5,HYDERABAD, KPHB COLONY,");
				System.out.println(yellow+space2+"\t                                   ROAD NUMBER-2, NEAR CV CORP INSTITUE");
				System.out.println(space2+yellow+"\t    ---------------------------------------------------------------------------");

				break; // Exit the loop if the OTP is valid
			} else {
				System.out.println("                                           Invalid OTP. Please try again.");
			}
		}
	}

	private int promptForOTP() {
		Scanner scanner = new Scanner(System.in);
		System.out.print("                                           Enter the OTP: ");
		return scanner.nextInt();
	}

}
abstract class ConfirmPassword 
{
	abstract void confirm();
}


