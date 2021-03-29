# ProjectRTMS
Finally did it ^___^

//******************************************************************************//
//	NAME 			: MUHAMMAD AKMAL BIN MOHD ADZUDDIN							                  //
//	ID	 			: 25350														                                //
//	PROGRAMME 		: ELECTRICAL AND ELECTRONICS ENGINEERING					            //
//	COURSE 			: EDB 4123 REAL TIME MICROCONTROLLER SYSTEMS (RTMS)	 		        //
//	LECTURER 		:	DR PATRICK SEBASTIAN									                        //
//	BATCH			: JANUARY 2021 												                            //	
//																				                                      //
//	PROJECT TITLE : DEFUSE THE BOMB (GAME)										                  //
//	FUNCTIONS UTILISED : 	1. LCD												                        //	
//							2. 7 SEGMENT (BLOCK 2 AND 3)						                        //
// 							3. KEYPAD											                                  //
//							4. 4 RED LEDs										                                //
//							5. RGB LEDs											                                //
//							6. BUZZER											                                  // 
//							7. ADC6 & ADC7 										                              //
//							8. TIMER0 TIMER1 TIMER3								                          //
//							9. RANDOM FUNCTION (SRAND RAND)					                        //
//																				                                      //
//																				                                      //
//	COPYRIGHTS : NONE, FEEL FREE TO USE AND ADJUST 								              //
//							 DO FOLLOW ME AT GITHUB.COM/MUHMDAKML			 	                    //
//							 THANK YOU ^___^								   	                            //
//******************************************************************************//


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
