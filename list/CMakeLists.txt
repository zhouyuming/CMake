cmake_minimum_required(VERSION 3.10)
project(main)
 
set(str1 hello world zhouyuming)
message(STATUS ${str1})

list(TRANSFORM str1 PREPEND -l)
message(STATUS ${str1})