# Chapter-functions
Functions and Dates 

#Functions
##x^n
make.power<-function(n){
  pow<-function(x){
    x^n
  }
  pow}
cube<-make.power(3)
square<-make.power(2)
cube(3)
square(3)

ls(environment(cube))
get("pow",environment(cube))

ls(environment(square))
get("n",environment(square))

#lexical vs dynamic scoping

y<-10
f<-function(x){
  y<-2
  y^2 + g(x)
  }
g<-function(x){
  x*y
}
f(3)

#Dates and times
x<-Sys.time()
x

p<-as.POSIXlt(x)
names(unclass(p))
p$sec

x<-Sys.time()
x
unclass(x)
x$sec
p<-as.POSIXlt(x)
p$sec

##change the format
datestring<-c("January 10,2012 10:40", "December 9, 2011 9:10")
f<-strptime(datestring,"%B %d, %Y %H:%M")
f
class(f)

x<-as.Date("2012-01-01")
y<-strptime("9 Jan 2011 11:34:21", "%d %b %Y %H:%M:%S")
x-y
x<-as.POSIXlt(x)
x-y
