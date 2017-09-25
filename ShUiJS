//make button work recieving files, setting value for test
var email1 = document.getElementById('email1');
var error = document.getElementById('error');
var correct = document.getElementById('correct');
var called = false; //only true when actually called


document.getElementById('email1').onkeydown = function(e){ //when enter is pressed on email address
   if(e.keyCode == 13){
       getEmail();
       return false; //this bugger I hadn't learned. Kept leaving instantly, need it to return false so values remain
   }
};



function getEmail(){ //actual function calling the email verifier
    called = true; //so it doesn't run on its own by accident, only when called
    reset(); //makes sure "please enter valid email and thanks for submitting aren't on at the same time"
    if (called == true){ 
        
        if (checkEmail(email1.value)){ //change text if email valid
           document.getElementById("correct").innerHTML = "Thanks for submitting. Check your email for updates!";
            
        }else{ //change text if email invalid
            document.getElementById("error").innerHTML = "Please enter a valid email address";
            
        }
    
    }
    

}

function reset(){  //resets as described in getEmail function.
               document.getElementById("correct").innerHTML = "";
               document.getElementById("error").innerHTML = "";
}



function checkEmail(email) { //just does a basic check for if there's text, then an @ sign, then text, then period, then text such as com. Ideally for a serious project I'd have a much better list such as checking .com, .ca , etc
    var re = /\S+@\S+\.\S+/;
    return re.test(email);
}




