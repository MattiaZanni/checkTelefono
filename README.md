# Check Telefono

Ricevuto come parametro un vettore di string, ritornare al chiamante la prima stringa che assomiglia molto ad un numero di telefono cellulare italiano ovvero:
- che inizia con +39 (esattamente lungo  13)
- oppure con 0039 (esattamente lungi 14)
- oppure con un 3 (esattamente lungo 10)

Se il numero non viene trovato, ritornare strunga vuota ""

Ad esempio.
Se arriva "05417373", "3367726712",  "778823"
Tornare "3367726712"

Se arriva "33677267", "33677232",  "778823"
Tornare ""

Se arriva "", "05417723",  "+391231231234"
Tornare "+391231231234"

Se arriva "3", "05417723",  "00391231231230"
Tornare ""




## **esercizio:**


using System;
using System.Collections.Generic;

public static class Telefono {
    public static string Check(string[] input) {
        
        for (int i = 0; i < input.Length; i++ ) {

            string num = input[i];

            if (
                (num.Length == 13 && num.StartsWith("+39")) ||
                (num.Length == 10 && num.StartsWith("3")) ||
                (num.Length == 14 && num.StartsWith("0039"))
                )

            {

                return num;

            }

        }

        return "";

    }
  }


