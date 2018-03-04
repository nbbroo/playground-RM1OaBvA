# Welcome!

This Java template lets you get started quickly with a simple one-page playground.

```java runnable
import java.util.*;
import java.io.*;
import java.math.*;

/**
 * Auto-generated code below aims at helping you parse
 * the standard input according to the problem statement.
 **/
class Solution {

    public static void main(String args[]) {
        // Scanner in = new Scanner(System.in);
        int L = 4;
        int H = 5;
        // in.nextLine();
        String T = "MANHATTAN";
     
        int longT = T.length(); 
        
        // tableau des lettres à afficher
        String lettre[] = new String[longT];
        // code ASCII des lettres à afficher
        int code[] = new int[longT];
        
        
        
        // charge les lignes construisant les lettres
        String ligne[] = new String[H];
        // charge les signes construisant LA LETTRE
        String dessinLettre[] = new String[H];
        // construit les lignes à afficher
        String dessinMot[] = new String[H];
     
          ligne[0] = " #  ##   ## ##  ### ###  ## # # ###  ## # # #   # # ###  #  ##   #  ##   ## ### # # # # # # # # # # ### ### ";
          ligne[1] = "# # # # #   # # #   #   #   # #  #    # # # #   ### # # # # # # # # # # #    #  # # # # # # # # # #   #   # ";
          ligne[2] = "### ##  #   # # ##  ##  # # ###  #    # ##  #   ### # # # # ##  # # ##   #   #  # # # # ###  #   #   #   ## ";
          ligne[3] = "# # # # #   # # #   #   # # # #  #  # # # # #   # # # # # # #    ## # #   #  #  # # # # ### # #  #  #       ";
          ligne[4] = "# # ##   ## ##  ### #    ## # # ###  #  # # ### # # # #  #  #     # # # ##   #  ###  #  # # # #  #  ###  #  ";
       
        /**
        for (int i = 0; i < H; i++) {
            
            String ROW = in.nextLine();
            ligne[i] = ROW;
          
        }
        **/

        for (int i=0; i<longT; i++){
        lettre[i]  = Character.toString(T.charAt(i));
        code[i] = T.charAt(i);
        
    if (code[i] > 96 && code[i] < 123){code[i]=code[i]-32;}
    if ((code[i] > 122 || code[i] < 96) && (code[i] < 65 || code[i] > 90)){code[i] = 63;}
        
    //    System.err.println(lettre[i] + ":" + code[i] +" / "+ (int)T.charAt(i) );     
       }
      
  // reconstruire la lettre
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
        // Write an action using System.out.println()
        // To debug: System.err.println("Debug messages...");
          for (int j=0; j < H ; j++ ) {
           System.out.println(dessinMot[j]);
        }

}}
```

# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced Java template](https://tech.io/select-repo/385)
