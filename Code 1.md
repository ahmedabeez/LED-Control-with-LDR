# LED-Control-with-LDR
//Develop the program to read values of LDR and display it on serial plotter. Now 
save this image and add in your lab report.

void setup() {
  Serial.begin(9600); // Setting up serial communication at 9600 bps
}
// Repeatedly reading and printing analog sensor values from pin A2 to Serial Monitor
void loop() {
  Serial.println(analogRead(A2)); // Print the analog sensor value
delay(100); // Delay for 100 microseconds
}

