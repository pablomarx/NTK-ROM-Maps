# Newton Toolkit ROM Maps

This repo contains decoded ROM Maps from Newton Toolkit 1.6.4.  The ROM maps were encoded using a simple substitution cipher.

The substitution values were found by searching the resource fork of NTK for 'abcdefg'.  A number of results were found, but one in the DATA resource was of particular interest.
It contained two ASCII lists, both NULL terminated, one starting at N and the other at A.  

![Screenshot of DATA resource hex dump in ResEdit](https://i.imgur.com/pZ4N8mS.png)

Using these values as-is produced decent results, but a number of characters were shifted by one.  This was due to the bottom list containing one byte more than the top, located at 05d166. Removing this byte resulted in a perfect decode. 
