# ProjectRTMS
Finally did it ^___^

NAME 			: MUHAMMAD AKMAL BIN MOHD ADZUDDIN
ID 			    : 25350
PROGRAMME 		: EE
COURSE 		    : EDB 4123 REAL TIME MICROCONTROLLER SYSTEMS JAN 2021
LECTURER 		: DR PATRICK SEBASTIAN 
DATE OF PROJECT DEMO : 25TH MARCH 2021


FUNCTIONS UTILISED:
1.	LCD = Show main menu, crosshair and bombs
2.	7 Segment (Block 2 and 3) = Show bomb countdown timer
3.	Keypad = User input (1/2/3 for choosing difficulty, 5 to defuse bomb or exit game)
4.	4 Red LEDs = Blink and speed according to difficulty level 
5.	RGB LEDs = Shows successful mission
6.	Buzzer = Sounds when mission is a success or a failure
7.	ADC6 and ADC7 (Internal and External Variable Resistors) = Control crosshair X-Y movements
8.	TIMER0 TIMER1 TIMER2 = Control 4 Red LEDs blinking speed
9.	RANDOM FUNCTION (SRAND / RAND) = Randomize set of bombs used



GAME FLOW:
•	Show Game Main Menu

•	Players choose which difficulty according to keypad input 1 or 2 or 3
    o	Recruit, 1 bomb, 30 seconds countdown timer
    o	Major, 2 bombs, 15 seconds countdown timer
    o	Veteran, 3 bombs, 10 seconds countdown timer
    
•	Program will initialize 
    o	Randomize bomb(s) position
    o	Arming the bomb(s)
    o	Set bomb countdown timer
    o	Set LED blinking speed based on Timer[x] (Interrupt)
    
•	Show Game Loading Screen
    o	LED loading strobe lights
    
•	Start Game
    o	Bombs will be shown
    o	Countdown timer will start
    o	Crosshair is shown
    o	Keypad 5 input to defuse the bomb
    o	If crosshair is within range of bomb && crosshair is within margin of defusing && keypad 5 is pressed:
        	The particular bomb(s) will be defused
    o	If all bombs defused:
        	Timer will stop and game ends with mission success
    o	If any bomb(s) not defused:
        	Timer will end and game ends with mission failure
        
•	End of Game
    o	Timers and LED is disabled
    o	LCD is cleared
    o	Show End Game Menu
        	Show how many times game has played
        	Options to replay again or exit

END OF GAME
