### Solved by AmirhoseinEjazi🔓😎😂

## Decrypted Message

> Congratulations! O brilliant codebreaker! You have unlocked the enigma and deciphered the hidden message.  
> May your mind be as sharp as the finest tool.  
> Now, venture forth and deposit your code at the secret repository.  
> Your journey has just begun...

##  My Decryption Script

```python
def caesar_decrypt(text, shift):
    result = ''
    for char in text:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base - shift) % 26 + base)
        else:
            result += char
    return result


ciphertext = """Gsrkvexypexmsrw0$S$fvmppmerx$gshifvieoiv%$]sy$lezi$yrpsgoih$xli$irmkqe$erh$higmtlivih$xli$lmhhir$qiwweki2$Qe}$}syv$qmrh$fi$ew$wlevt$ew$xli$jmriwx$xssp2$Rs{0$zirxyvi$jsvxl$erh$hitswmx$}syv$gshi$ex$xli$wigvix$vitswmxsv}2$]syv$nsyvri}$lew$nywx$fikyr%$Jsv$xlswi${ls$lezi$higmtlivih$xlmw$q}wxiv}0$gsrkvexypexmsrw%$Tpiewi$qeoi$wyvi$xs$wyfqmx$}syv$gshi$zme$e$typp$viuyiwx$ex$lxxtw>33kmxlyf2gsq3ELQ1MH3Gv}txskvetl}1Tviwirxexmsr$erh$nsmr$syv$gsqqyrmx}$sj$gshifvieoivw2"""

for i in range(1, 26):
    decrypted_text = caesar_decrypt(ciphertext, i)
    print('#'*30)
    print(decrypted_text)