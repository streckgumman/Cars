import java.awt.*;

public class Cars{

    private final int nrDoors; // Number of doors on the car
    private final double enginePower; // Engine power of the car
    private double currentSpeed; // The current speed of the car
    private final Color color; // Color of the car
    private final String modelName; // The car model name


    private double x;
    private double y;
    private double dx;
    private double dy;
    
    public Cars(int nDoors, Color color, int enginePower, String modelName, double currentSpeed){
        this.nrDoors = nDoors;
        this.color = color;
        this.enginePower = enginePower;
        this.modelName = modelName;
        this.currentSpeed = currentSpeed;
    }


    public void move(){
	if (direction.equals(Direction.NORTH)){
	    setCurrentPoint(new Point(currentPoint.x, currentPoint.y + currentSpeed;
	}
	if (direction.equals(Direction.SOUTH)){
	    setCurrentPoint(new Point(currentPoint.x, currentPoint.y - currentSpeed;
	}
	if (direction.equals(Direction.WEST)){
	    setCurrentPoint(new Point(currentPoint.x + currentSpeed, currentPoint.y;
	}
	if (direction.equals(Direction.NORTH)){
	    setCurrentPoint(new Point(currentPoint.x  - currentSpeed, currentPoint.y;
	}

    }
    


    public void turnLeft(){
	if (direction.equals(Direction.NORTH)){
	    direction = Direction.WEST;
	}
	else{
	    direction = Direction++;
	}
    }

    public void turnRight(){
	if (direction.equals(Direction.EAST)){
	    direction = Direction.NORTH;
	}
	else{
	    direction = Direction--;
	}
    }





    
    public int getNrDoors(){
        return nrDoors;
    }
    public double getEnginePower(){
        return enginePower;
    }

    public double getCurrentSpeed(){
        return currentSpeed;
    }

    public Color getColor(){
        return color;
    }

    public void setColor(Color clr){
	    color = clr;
    }

    public void startEngine(){
	    currentSpeed = 0.1;
    }

    public void stopEngine(){
	    currentSpeed = 0;
    }
    
    public double speedFactor(){
        return enginePower;
    }

    public void incrementSpeed(double amount){
	currentSpeed = getCurrentSpeed() + speedFactor() * amount;
    }

    public void decrementSpeed(double amount){
        currentSpeed = getCurrentSpeed() - speedFactor() * amount;
    }

    // TODO fix this method according to lab pm
    public void gas(double amount){
        incrementSpeed(amount);
    }

    // TODO fix this method according to lab pm
    public void brake(double amount){
        decrementSpeed(amount);
    }




/*
    int getNextPlayerNum(Player[] players, int currPlayNum) {

        if (currPlayNum >= players.length - 1) {

            return 0;

        }

        return ++currPlayNum;

    }


*/




}
