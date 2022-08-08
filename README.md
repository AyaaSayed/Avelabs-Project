# Avelabs-Project
#In this project, you are supposed to implement an application that generates a software PWM using a software PWM driver.



Please use this datasheet as your guide through your implementation.



Suppose you have the GPIO/DIO driver that has the following APIs:

#define IN 0
#define OUT 1
#define LOW 0
#define HIGH 1

/*
 * pinNumber: is an input argument that describes the pin number in each port, 0, 1, 2, ... etc.
 * port: is an input argument that describes port character, 'A', 'B', ... etc.
 * direction: is an input argument that describes the data direction on a specific pin, IN or OUT
 */
 void DIO_init(uint8_t pinNumber, uint8_t port, uint8_t direction);
 
 /*
 * pinNumber: is an input argument that describes pin number in each port, 0, 1, 2, ... etc.
 * port: is an input argument that describes port character, 'A', 'B', ... etc.
 * value: is an input argument that describes the value on a specific pin, LOW or HIGH
 */
 void DIO_write(uint8_t pinNumber, uint8_t port, uint8_t value);
 
 /*
 * pinNumber: is an input argument that describes pin number in each port, 0, 1, 2, ... etc.
 * port: is an input argument that describes port character, 'A', 'B', ... etc.
 */
 void DIO_toggle(uint8_t pinNumber, uint8_t port);
 

Use PIN 0 in port A as the PWM pin for the SW PWM driver.

You should implement the following SW PWM APIs:

/*
 * frequency_kh: is an input argument that describes the frequency in KHz.
 * dutyCycle: is an input argument that describes the duty cycle needed for the PWM that varies from 0 to 100 ( 0 means 0%, and 100 means 100%).
 */
 void SWPWM_init(uint32_t frequency_kh, uint8_t dutyCycle);

/*
 * This function is to start PWM generation.
 */
 void SWPWM_start(void);
 
/*
 * newDutyCycle: is an input argument that describes the new duty cycle needed for the PWM.
 */
 void SWPWM_changeDutyCycle(uint8_t newDutyCycle);
 
 /*
 * This function is to stop PWM generation.
 */
 void SWPWM_stop(stop);

Requirements
Implement an application that will generate a PWM signal that changes from 0% duty cycle to 100% duty cycle with a 1% step
Each step will take 1ms
The PWM has a 1KHz frequency


What to deliver
Timer driver, TIMER_init, TIMER_set, TIMER_start, TIMER_stop, and TIMER_getstate, for each timer you use
The SW PWM driver
The application
 

How to submit
Please upload the code for this project to GitHub, and post a link to your repository below.



Note
This project must be submitted during the assessment time.
