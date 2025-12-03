Follow up from previous process injection experiment

This C code allocates an encrypted null terminated string as shellcode, spawns svchost suspended, typical injection stuff.

This time however, there are NO imports from the Kernel32.dll. There is a handle to it, however through a technique called 'Dynamic API resolution' I defined my own functions, and pointed them to a memory location to call the Windows API without any import headers.

This resulted in a 12% decrease in EDR/AV detections when measured with VirusTotal.
