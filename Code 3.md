//Develop a program which controls the brightness of LED with the help of an 
LDR and display its reading on serial monitor/serial plotter. For Case 2, LED 
should turn OFF when it’s dark

int mp;  //variable to store analog sensor readings
int cake;  //variable to store raw sensor value 
void setup()  // put your setup code here, to run once:
{
pinMode(6,OUTPUT);  //set pin 6 as an output
Serial.begin(9600);  //begin a baud rate at 9600 bps
}
void loop()  // put your main code here, to run repeatedly:
{
cake = analogRead(A2);  //read the analog input from pin A2
Serial.print("LDR i/p value is: ");  //print the sensor value to the serial monitor
Serial.println(cake); //print value that is stored in variable “cake”
mp = map (cake , 0, 1023, 0 ,255); // Map the sensor value from the range 0-1023 to 0-255
analogWrite(6, mp);  // Set the brightness of the LED connected to pin 6 based on the mapped value
Serial.print("LED value is: "); //print the LED brightness value to the serial monitor 
Serial.println (mp); //print the value that is stored in variable
Serial.println("");  // Print an empty line for better readability in the Serial Monitor
delay (1000); //delay for 1 microseconds
}
