# romanToInteger
conversion of roman numerals to integer
java

class Solution {
    public int romanToInt(String s) {
        int len=s.length();
        int sum=0;
        char ch,ch1;
        for(int i=0;i<len;i++)
        {  ch=s.charAt(i);
         

            if(ch=='I')
            {   
               if(i+1<len)
            { ch1=s.charAt(i+1);
          
                if(ch1=='V')
                {sum=sum+5-1;
                i++;
                continue;}
                
                if(ch1=='X')
                {sum=sum+10-1;
                i++;
                continue;}
            
         }
            
             
               sum=sum+1;
                
            }
             
            if(ch=='V')
            { 
                sum=sum+5;
            }
            if(ch=='X')
            {  if(i+1<len)
         { ch1=s.charAt(i+1);
         
                if(ch1=='L')
                {sum=sum+50-10;
             i++;
                continue;}
                
                if(ch1=='C')
                {sum=sum+100-10;
                i++;
                continue;}
         }
              
                sum=sum+10;
            }
            if(ch=='L')
            {
                sum=sum+50;
            }

            if(ch=='C')
            {if(i+1<len)
         { ch1=s.charAt(i+1);
         
                if(ch1=='D')
                {sum=sum+500-100;
                 i++;
                continue;}
                
                if(ch1=='M')
                {sum=sum+1000-100;
                i++;
                continue;}
         }
                
                sum=sum+100;
            }
            if(ch=='D')
            {
                sum=sum+500;
            }
            if(ch=='M')
            {
                sum=sum+1000;
            }
            
            
        }
        return sum;
        
    }
}
