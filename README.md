# AssemblyRecursion
Implemented this in ARM:

  int F(int i, int j, int k)
  {
     
     
     int s, t;

     if ( i <= 0 || j <= 0 )
        return(-1);
     else if ( i + j < k )
        return (i+j);
     else
     {
        s = 0;
        for (t = 1; t < k; t++)
        {
           s = s + F(i-t, j-t, k-1) + 1;               
        }
        return(s);
     }
  }
