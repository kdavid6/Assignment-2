# Assignment-2


public class Car {
	int gear = 1;
	int location;
	int speed = 0;
	final int DESTINATION = 250;
	 
	
	void reverseGear(){
		gear = -1; 
		
	}
	
	void gearUp(){
		if(gear == 6){
			System.out.println("Cannot increase the gear anymore"); 
		}
		else if(gear == -1){
			gear = 1;
		}
		else{
			gear = gear + 1;
		}
			
				
	}
	void gearDown(){
		if(gear == 1){
			System.out.println("Cannot decrease the gear anymore");
		}
		else if(gear == -1){
			System.out.println("Cannot decrease the gear");
			
		}
		
	}
	int reportGear(){
		return gear;
	}
	int reportLocation(){
		return location;
	}
	int reportRemaining(){
		return DESTINATION - location;
		
	}
	void moveByTime(int time){
		int delta;
		if(time < 0){
			System.out.println("Time should be positive");
		}
		else
		{
			speed = gear * 20;
			delta = speed * time;
			location = location + delta;
		}
	}
	boolean isArrived(){
		if(location >= DESTINATION){
			return true;
		}
		else{
			return false;
		}
	}
	
}
