# Learn how to achieve Debouncing



###    Title       : Debouncing
####   Author      : Prakhar Mathur
####   Designation : UI Developer
####   Date        : 23 Nov 2019
  
       Description : What happend here when we try to call debounce method setTimeout method
                 Calls and because of the wait ie: time delay it can not fire function immediately
                 it holds function until the time of delay not completed
                 then suddendly we call another debounce method then debounce method reads clearTimeout 
                 method it clear all the timeout 
                 again setTimeout method sets and holds function till delay time not completed
                 Once the delay completed it fires the function fn               
 


###### function debounce(fn,w) {
 ######    var timeout;
 ######    return function() {  
 ######        later = ()=>{    
  ######          //apply request here;
  ######           fn();
 ######        }
  ######       clearTimeout(timeout);
   ######      timeout = setTimeout(later,w);        
   ######      console.log(timeout)
   ######  }   
###### };

 ######var myEfficientFn = debounce(function() {
 ######	console.log("Debouncing Achieved")
 ######}, 250);
