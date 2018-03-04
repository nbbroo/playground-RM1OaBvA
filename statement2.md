# we love ASCII ART

```java runnable

import java.util.*;
import java.io.*;
import java.math.*;

class Main {

    public static void main(String args[]) {
    
           //##################################################    
 String T = "WE LOVE"; // <--- Write your text here #
           //##################################################

        int longT = T.length(); 
        int L = 10;
        int H = 8;

        String lettre[] = new String[longT];
        int code[] = new int[longT];
        String ligne[] = new String[H];
        String dessinLettre[] = new String[H];
        String dessinMot[] = new String[H];
     
          ligne[0]="          _                  _           __           _       _     _   _      _                                                            _                                                   ";
          ligne[1]="         | |                | |         / _|         | |     (_)   (_) | |    | |                                                          | |                                                  ";
          ligne[2]="   __ _  | |__     ___    __| |   ___  | |_    __ _  | |__    _     _  | | __ | |  _ __ ___    _ __     ___    _ __     __ _   _ __   ___  | |_   _   _  __   __ __      __ __  __  _   _   ____";
          ligne[3]="  / _` | | '_ \   / __|  / _` |  / _ \ |  _|  / _` | | '_ \  | |   | | | |/ / | | | '_ ` _ \  | '_ \   / _ \  | '_ \   / _` | | '__| / __| | __| | | | | \ \ / / \ \ /\ / / \ \/ / | | | | |_  /";
          ligne[4]=" | (_| | | |_) | | (__  | (_| | |  __/ | |   | (_| | | | | | | |   | | |   <  | | | | | | | | | | | | | (_) | | |_) | | (_| | | |    \__ \ | |_  | |_| |  \ V /   \ V  V /   >  <  | |_| |  / / ";
          ligne[5]="  \__,_| |_.__/   \___|  \__,_|  \___| |_|    \__, | |_| |_| |_|   | | |_|\_\ |_| |_| |_| |_| |_| |_|  \___/  | .__/   \__, | |_|    |___/  \__|  \__,_|   \_/     \_/\_/   /_/\_\  \__, | /___|";
          ligne[6]="                                               __/ |              _/ |                                        | |         | |                                                        __/ |      ";
          ligne[7]="                                              |___/              |__/                                         |_|         |_|                                                       |___/       ";
          
        for (int i=0; i<longT; i++){
        lettre[i]  = Character.toString(T.charAt(i));
        code[i] = T.charAt(i);
        
    if (code[i] > 96 && code[i] < 123){code[i]=code[i]-32;}
    if ((code[i] > 122 || code[i] < 96) && (code[i] < 65 || code[i] > 90)){code[i] = 63;}
       }
 
       int rang;
       for (int comp=0; comp<H; comp++){dessinMot[comp]="";}
       for (int r=0; r<longT;r++){
       rang = (code[r]-65) * L;
       if (rang<0){rang=26*4;}
       for (int j=0; j < H ; j++ ) {

          dessinLettre[j] = ligne[j].substring(rang,rang+L);
          dessinMot[j] = dessinMot[j] + dessinLettre[j];
       
        }
        }
          for (int j=0; j < H ; j++ ) {
           System.out.println(dessinMot[j]);
        }

}}
```
# Try your self
