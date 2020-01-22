# STM32F446-CAN_BUS
STM32F446 reading voltage from RoboteQ MDC2460 brushed motor driver through CAN bus. 

The selected CAN Mode is : CANopen !

Some notes: The Can_Id of RoboteQ is 0x08 , to read the voltage from the driver you have to send 0x210D.

The frame that is sent is composend from the followings:
TxHeader.DLC = 8 => Data length = 8 bytes
TxHeader.StdId = 0x600 | 8 

In order to understand TxHeader.StdId, you need to understand how CANopen mode works.
Here's a link for more details: https://doc.ingeniamc.com/emcl2/command-reference-manual/communications/canopen-protocol

![](images/table.png)

The CAN1_TX and CAN1_RX is connected to a CAN tranceiver which in turn is connected to the driver.

See the Logic analyzer screenshot for more information. 
