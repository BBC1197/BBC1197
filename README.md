import java.util.*;
public class Main {


	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Hotel h=new Hotel();
		String aroom="yes";
		Scanner sc=new Scanner(System.in);
		System.out.println("Enter the Hotel details:");
		System.out.println("Enter the Hotel Name:");
		String h_name=sc.nextLine();
		System.out.println("Enter the Hotel ID:");
		String h_id=sc.nextLine();
		System.out.println("Enter the Hotel Address");
		String h_add=sc.nextLine();
		do
		{
			System.out.println("Enter the Room Details:");
			System.out.println("Enter the Room Id:");
			String roomid=sc.nextLine();
			System.out.println("Enter the Room Number:");
			String roomno=sc.nextLine();
			System.out.println("Enter the Room Type:\n1)Normal\n2)Delux\n3)Super Delux");
			String roomtype=sc.nextLine();
			if(roomtype.equals("1"))
			{
				roomtype="Normal";
			}
			else if(roomtype.equals("2"))
			{
				roomtype="Delux";
			}
			else if(roomtype.equals("3"))
			{
				roomtype="Super Delux";
			}
			
			System.out.println("Enter the Room Capacity:(1/2/3/4)");
			String roomcapa=sc.nextLine();
			System.out.println("AC Service (true/false):");
			String roomac=sc.nextLine();
			System.out.println("Wi-Fi Service (true/false):");
			String roomwifi=sc.nextLine();
			System.out.println("Cable Service (true/false):");
			String roomcab=sc.nextLine();
			System.out.println("Laundry Service (true/false):");
			String roomlan=sc.nextLine();
			System.out.println("Do you want to add Another Room (yes/no):");
			aroom=sc.nextLine();
			Room r=new Room(roomid,roomtype,roomno,roomcapa,roomac,roomwifi,roomcab,roomlan);
			h.addRoom(r);
			
			
		}
		while(aroom.equals("yes"));
		
		if(aroom.equals("no"));
		{
			System.out.println("Thank you for booking !!");
			System.out.println("The rooms Details in "+h_name +" :");
			System.out.println("Hotel Name:"+h_name+".");
			System.out.println("Hotel ID:"+h_id+".");
			System.out.println("Hotel Address:"+h_add+".");
			System.out.println("\nRoom Details:\n");
			Collections.sort(h.robj,new CompareSorting());
			h.display();
		}
	}

}  
................
