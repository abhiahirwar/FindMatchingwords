import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.regex.*;

class Result {

   
    public static String findMatchingWords(String[] strArray) {
  
      String matcher ="";
      String result = "";
      
      for(int i=0; i < strArray.length; i++) 
      {
        matcher += strArray[i];
      }
      
      char[] matcherArray = matcher.toCharArray();
    
      for(int j=0; j < strArray.length; j++) 
      {
       for(char c:matcherArray) {
         int index = strArray[j].indexOf(c);
         if( index >= 0 ) {
           result += c;
         }
         
       }
       
       result ="";
      }
      
      for(char c : matcherArray) 
      {
      boolean flag = true;
        
      for(int j=0; j < strArray.length; j++) 
      {
          if( (strArray[j].indexOf(c)  >= 0) && flag ) 
          {
            flag = true;
          } else 
          {
            flag = false;
          }
        }
        if(flag) 
        {
          result += c;
        }
      }
      
      return  removeDuplicate(result.toCharArray(), result.toCharArray().length); 
   }
    
    public static String removeDuplicate(char[] str, int n) 
    { 
 
        int index = 0; 
  
  
        for (int i = 0; i < n; i++) 
        { 
            int j; 
            for (j = 0; j < i; j++)  
            { 
                if (str[i] == str[j]) 
                { 
                    break; 
                } 
            } 
  
            if (j == i)  
            { 
                str[index++] = str[i]; 
            } 
        } 
        return String.valueOf(Arrays.copyOf(str, index)); 
    } 

}

public class Solution1{
    public static void main(String[] args) {
      
      String[] test1 = new String[]{"flower","flow","flight"};
        String[] test2 = {"dog","dr","dlight"};
        
        String result1 = Result.findMatchingWords(test1);
        String result2 = Result.findMatchingWords(test2);
        
        System.out.println(result1);
        System.out.println(result2);
    }
}
