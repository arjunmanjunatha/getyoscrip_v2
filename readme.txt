let us build a html page with a web form. The title of this page in bold and centered should be "Get Yo Scrip". The heading under the table should be "input your details". 
First question on the form should be: AID and a text input box for the user to type in a set of letters and numbers. 
The second question should be "Exclude Providers" and the input should be 7 options with checkboxes. The first option is ALL (Pop only). The second option is Booking. The third option is Expedia. The third option is VRBO. The fourth option is hotelscom. The fifth option is tripadvisor. The sixth option is hotelscombined The seventh option is none and should be checked by default. The user can check multiple options, except the first and last together. The output of the form will change based on the choice made in this question. 

The third question on the form should be "Grab existing links from" and the input should be 4 options with three of them being checkboxes. The first option should be none and checked by default. The second option should be a checkbox "CJ". The third option should be a checkbox "TravelPayouts". The fourth option should be a text input field titled "custom". This text field should accept a url with at least one dot and one slash. 

After this question, there should be a big submit button and it should trigger the output. 

The output must be a javascript snippet inside a code box that a user can copy, similar to what chatgpt responses have. 

The output is this javascript snippet, and lines on it are modified depending on the answers from the form: 
<script>
  (function (s, t, a, y, twenty, two) {
    s.Stay22 = s.Stay22 || {};

    // Just fill out your configs here
    s.Stay22.params = {
      aid: "YOUR_AID_GOES_HERE_INSIDE_QUOTES", // your partner ID for tracking, keep quotes
    };

    // Leave this part as-is;
    twenty = t.createElement(a);
    two = t.getElementsByTagName(a)[0];
    twenty.async = 1;
    twenty.src = y;
    two.parentNode.insertBefore(twenty, two);
  })(window, document, "script", "https://scripts.stay22.com/letmeallez.js");
</script>

The answer from the first question on the form should be the input that replaces YOUR_AID_GOES_HERE_INSIDE_QUOTES for the parameter aid. This is a compulsory question and has to have an input. 

For the second question, if the response is the first option ALL (pop only), then add this line with this array: excludes: ["vrbo","booking","expedia","tripadvisor","hotelscombined","hotelscom"] after the line with aid: "YOUR_AID_GOES_HERE_INSIDE_QUOTES". 

Then if the responses include checking the second, third, fourth, fifth or 6th option, add them to the array defined in excludes: ["vrbo","booking","expedia","tripadvisor","hotelscombined","hotelscom"]

If the response is the seventh option None, then don't add any modifications for the script output. 

For the third question, if the response is none then don't add any modifications for the script output. If the response is CJ, then add this line after in the params: 
 deepStruct: ["fave.co/","anrdoezrs.net/click","kqzyfj.com/click","dpbolvw.net/click","tkqlhce.com/click","jdoqocy.com/click"]

If the response is third option TravelPayouts, then add this line in the params instead:  deepStruct: ["tp.st/","tp.media/"]

If the response is both travelpayouts and CJ, then add this line to the params: deepStruct: ["fave.co/","anrdoezrs.net/click","kqzyfj.com/click","dpbolvw.net/click","tkqlhce.com/click","jdoqocy.com/click","tp.st/","tp.media/"]

If the response is an input into the fourth option, then add that input as the variable in a new line after aid. This is the required line of code
 deepStruct: ["input_option_here"] 

The user's button to copy the output code snippet should be on the top right of the box. 
