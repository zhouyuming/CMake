
cmake_minimum_required(VERSION 3.10)
project(main)
 
set(str1 "hello")
message(STATUS ${str1})
 
set(str2 "world")
message(STATUS ${str2})
 
string(APPEND str1 " ${str2}")
message(STATUS ${str1})
 
string(APPEND str1 "!!!")
message(STATUS ${str1})