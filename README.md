Follow up from previous process injection experiment

This C code allocates an encrypted null terminated string as shellcode, spawns svchost suspended, typical injection stuff.

This time however, there are NO imports from the Kernel32.dll. There is a handle to it, however through a technique called 'Dynamic API resolution' I defined my own functions, and pointed them to a memory location to call the Windows API without any import headers.

This resulted in a 12% decrease in EDR/AV detections when measured with VirusTotal.

SHA-256 Hash:
37a9958ff370c8321a8f8995556f7a13074c2940f27f3841e5c120d53d56201e
