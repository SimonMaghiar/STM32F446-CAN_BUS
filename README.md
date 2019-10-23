# STM32F446-CAN_BUS
STM32F446 reading voltage from RoboteQ MDC2460 brushed motor driver through CAN bus. 

Some notes: The Can_Id of RoboteQ is 0x08 , to read the voltage from the driver you have to send 0x210D.

The CAN1_TX and CAN1_RX is connected to a CAN tranceiver which in turn is connected to the driver.

See the Logic analyzer screenshot for more information. 
