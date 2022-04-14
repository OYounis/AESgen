# AESgen
[The Advanced Encryption Standard (AES)](https://en.wikipedia.org/wiki/Advanced_Encryption_Standard) is the primary symmetric encryption and decryption mechanism used in many applications.
***
The AESgen is a python based AES core generator that is designed to support [AES-NI](https://en.wikipedia.org/wiki/AES_instruction_set) instructions and is therefore built to be encapsulated with a processor core in a single package. It has a simple ready-valid interface that can be easily extended.

The generator and base core are designed to support various customizations.
***
## Generator Features
- [ ] Support AES-ISA and two additional instructions
- [ ] Option for 128- , 256-bit key length..
- [ ] Full encryption modes support (ecb, cbc, gcm, etc.).
- [ ] Encryption-only, Decryption-only, Full Operation.
- [ ] Support for microarchitecture level configurations:
    - [ ] Option for 32- , 64- , 128-bit datapaths.
    - [ ] Choose between T-box and S-box. 
    - [ ] LUT or composite-field tables.
    - [ ] Interface protocols (APB, AXI, Wishbone, etc.).
    - [ ] Pipelining (multiple physical rounds) and Sub-pipelining (single physical round).
***
### Supported Instructions
|Mnemonic| Description|
|---------|------------|
|NOOP|No Operation|
|AESENCFULL|Full Encryption|
|AESDECFULL|Full Decryption|
|[AESDEC](https://www.felixcloutier.com/x86/aesdec)|Decrypt Round|
|[AESDECLAST](https://www.felixcloutier.com/x86/aesdeclast)|Decrypt Last Round|
|[AESENC](https://www.felixcloutier.com/x86/aesenc)|Encrypt Round|
|[AESENCLAST](https://www.felixcloutier.com/x86/aesenclast)|Encrypt Last Round|
|[AESIMC](https://www.felixcloutier.com/x86/aesimc)|InvMixColumn Transformation|
|[AESKEYGENASSIST](https://www.felixcloutier.com/x86/aeskeygenassist)|Generate Round Key|

***
## References
The work in this project is heavily based on the following papers:
* [Satoh et al.](https://www.researchgate.net/publication/225127628_A_Compact_Rijndael_Hardware_Architecture_with_S-Box_Optimization), "A Compact Rijndael Hardware Architecture with S-Box Optimization"
* [Nabihah Ahmad, S.M. Rezaul Hasan](https://www.researchgate.net/publication/259118946_Low-power_compact_composite_field_AES_S-BoxInv_S-Box_design_in_65_nm_CMOS_using_Novel_XOR_Gate), "Low-power compact composite field AES S-Box/Inv S-Box design in 65nm CMOS using Novel XOR Gate"

