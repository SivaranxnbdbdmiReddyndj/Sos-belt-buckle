
Emergency GPS Tracker with GSM Call & SMS Notification

This project is a button-activated GPS tracker that uses a GSM module (like SIM800 or Quectel EC200U) to:

Call a predefined phone number

Send live GPS location via SMS every 5 minutes

Stop tracking if the button is held for 5 seconds


Features

Real-time GPS Location: Extracts latitude and longitude from NMEA sentences.

Google Maps Link: Sends an SMS with a direct link to the user's live location.

Emergency Call: Initiates a call to a parent/guardian on button press.

Failsafe Stop: Holding the button for 5 seconds stops tracking and ends the call.


Hardware Required

esp32

GSM Module (SIM800L, EC200U, or A9G with GPS)

Push Button

Jumper Wires

Power Supply (Battery or Adapter)

SIM Card (with SMS and call balance)

 
How  it works

1. Press Button Briefly: Starts tracking, calls the parent, and sends GPS location via SMS.


2. Send GPS SMS every 5 minutes: Keeps updating the parent with the latest position.


3. Hold Button for 5 seconds: Ends the call and stops location tracking.



Code Highlights

Uses SoftwareSerial to communicate with the GSM module.

Parses NMEA strings like $GPGGA or $GPRMC to extract GPS coordinates.

Converts coordinates to decimal degrees and embeds them into a Google Maps link.


Usage

1. Replace phone_number in the code with your parent’s number.


2. Upload the code using the Arduino IDE.


3. Insert a valid SIM card into the GSM module.


4. Power the device and press the button to initiate tracking.



Example SMS

📍 Location: https://www.google.com/maps?q=10.827908,77.0605168

Future Improvements

Add fall detection using an accelerometer

Use a low-power microcontroller (e.g., ATmega328P) for battery optimization

Integrate with a cloud dashboard via MQTT


