# Go lang String, Byte, Rune

Understanding the data type of any programming language will brighten your knowledge of it. 

Go is being used very widely. Go lang supports all the major data types. I tried to put my understanding about Rune, Byte and String in this article. 

# Byte : 

In Go lang Byte is of type uint8 . Each stores 8 bits of unsigned integers.


# String :

  A string is a sequence of any valid UTF-8 characters. The string is of Type uint8 ( unsigned integer 8 bits ).
  
    
      package main

      import "fmt"

      func main(){
        var hero string= "Tom"
        fmt.Printf("String Value = %v &  String Type = %T", hero, hero) 
        // result String Value = Tom & String Type = String
        fmt.Printf("String Value = %v &  String Type = %T", hero[0], hero[0) 
        // result String Value = 82 & String Type = unit8
      }

  Above, when we try to read the 0 index character, we can see the result appears as byte value 82. 
  String values are immutable, there is no possible way to assign a new value in the string either through the byte code or character.

# Rune : 

A Rune is for storing a single Unicode codepoint ( which is a unique number for each character ). Rune is of type int32 ( signed integer 32 bits ). When you assign some character to the rune variable it will store the unicode value of that character.

 
      package main
      import "fmt"

      func main(){
        var hero rune = 'T'
        fmt.Printf("Rune Value = %v &  Type = %T", hero, hero) // result Rune Value = 82 & Type = Rune
      }



# What is uint8, uint16, uint32, uint64 ?
unsigned integer only allows positive numbers.
  
# What is int8, int16, int32, int64 ?
signed int value can be either positive or negative numbers
