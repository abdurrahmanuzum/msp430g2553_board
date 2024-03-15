MSP430G2553 board with CH340 USB-UART bridge for programming.

**This board cannot do proper debugging.**

For programming script, see: https://github.com/gbhug5a/MSP430-BSL/tree/master

Can be run with the command: `<script_path>\BSLDEMO-2.01c.exe -cCOM<port#> -m1 -ijevpr <TI_HEX_filename.txt>`

Or can be embedded into the Code Composer Studio as a post-build step. Change the `<TI_HEX_filename.txt>` to `${BuildArtifactFileBaseName}.txt`. This will make the "Build" button to flash the program after building. (If building actually occurs, remember that the IDE will not build the identical project twice unless forced to. "nothing to build...")

CCS doesn't generate the output file by default, do: Project -> Properties -> Build -> MSP430 HEX Utility -> (1) Tick Enable 'MSP430 Hex Utility' -> Output Format Options -> (2) Select Output format: "TI-TXT hex --ti_txt"
