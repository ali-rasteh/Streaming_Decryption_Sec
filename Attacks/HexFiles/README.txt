*******************  README.txt  *******************
  
	This folder includes binaries which are updated to faciliate ChipWhisperer Attacks, 
	specifically CPA on AES. The changes includes using an external clock, providing a 
	scope trigger, and ensuring there are no background operations during encryption and 
	decryption. The files and protocols are as follows:

*********************  FILES  **********************  

	binary1.hex - Hex Binary 1 for the STMF0 Target on ChipWhisperer
	binary2.hex - Hex Binary 2 for the STMF0 Target on ChipWhisperer
	binary3.hex - Hex Binary 3 for the STMF0 Target on ChipWhisperer
	binary4.hex - Hex Binary 4 for the STMF0 Target on ChipWhisperer

*******************  Protocol  ********************* 

	** Important **
	Note that the AES protocol was slightly changed: it now does and AES ENCRYPT
	instead of the previously defined AES DECRYPT in the project specification.

	Protocol Bytes are identical to the project specification, except that the 
	0x30 protocol byte now refers to AES Encrypt as follows:

	0x10 - NOP
	0x20 - XOR Decrypt
	0x30 - DES Decrypt
	0x40 - AES Encrypt

	The response is identical to the project specification, as the MCU will return 
	17 bytes with the leading byte being success byte.
