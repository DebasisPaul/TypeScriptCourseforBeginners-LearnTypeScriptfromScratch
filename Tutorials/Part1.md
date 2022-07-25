
# Part 1 Start


# Introduction

0:00
my name is Debasis Paul and I will be your instructor in this course now this course is about typescript
0:07
superset to JavaScript so a programming language which actually builds up on JavaScript you could say it takes
0:14
JavaScript to the next level with typescript you will see in this course you can write less error-prone much
0:21
better and cleaner code and also use some exciting new features which don't exist like this in JavaScript now in
0:28 
this course you will learn typescript from scratch you don't need to know anything about types good to get started
0:34
basic JavaScript knowledge absolutely suffices you will learn all the basics
0:39
of typescript how it works why we use it the different advantages it offers we'll
0:45
dive into the core types it provides and will gradually build up knowledge and
0:50
dive into more and more advanced types good features throughout this course now this course is both a course that
0:57
focuses on the theory and showing a broad variety of features as well as
1:03
showing all these features in action and reall projects therefore in this course we'll have a real project we'll also
1:10
have a module where we dive into typescript with react we'll also have a module where we dive into typescript
1:17
with node and express so that by the end of this course you really feel comfortable using types could in your
1:23
next projects and that you know why you would use it and most importantly how you would apply it to any JavaScript
1:31
project you're working on no matter by the way if that is javascript in the
1:36
browser with or without any framework or if it's on the server-side so that's all
1:41
in the course I'm super excited to start this journey together with you and with that I'd say let's not waste any time
1:48
and let's find out what exactly types code is and which advantages it has to offer

# Part1 Start
1:59
so what is typescript what is it all about why would we use it typescript is
2:05
a JavaScript superset now what does this mean it means that typescript is in the
2:11
end a language a programming language building up on JavaScript it's not a
2:16
brand new language instead it takes the JavaScript language and adds new
2:22
features and advantages to it it makes writing JavaScript code easier and more
2:28
powerful you could say but we have one huge disadvantage typescript can't be
2:34
executed by JavaScript environments like the browser browsers can't execute
2:40
typescript and for example node.js also can't execute typescript so the
2:46
environments where we can execute JavaScript don't support typescript what's the idea behind typescript then


2:53
it's a better version of JavaScript and we can't use it well not quite
2:59
typescript is a programming language but it's also a tool it's a powerful
3:04
compiler which you run over your code to compile your typescript code to
3:10
JavaScript so what you get as a result when writing code in typescript is
3:16
JavaScript but you didn't write that JavaScript code you wrote typescript
3:21
code with all the new features and all the advantages and you get normal JavaScript code well that of course
3:28
brings up one important question how can types could add new features if what you
3:34
get in the end is regular JavaScript and the answer is the typescript compiler
3:40
compiles these new features to JavaScript workarounds so in the end it
3:45
might give you a nicer syntax an easier way of doing something and it will then
3:51
compile that nicer easier way to a more complex JavaScript snippet which you
3:57
would have to write otherwise so it's not magic of course it can't add what's
4:02
not possible at all in the JavaScript language but it can add new features
4:08
that simply are easier to use nicer syntax things like this in dition types of course that's one
4:15
important thing which the name already implies it adds types it adds a feature
4:21
to D JavaScript language ed which will have a close look in a second which will
4:26
actually give you as a developer an opportunity of identifying errors in
4:32
your code earlier before your script runs and the error occurs at runtime in
4:37
the browser so it does not only give you some new features and nicer ways of doing something it also gives you extra
4:46
error checking where errors which you would otherwise get as runtime errors
4:51
can be caught and fixed early during development so why would we use
4:56
typescript consider this example a fairly simple JavaScript function which
5:02
adds two numbers now when I call it please notice that I'm passing in two strings instead of two numbers and I'll
5:09
show you a real example where something like this could happen realistically in just a second so we're calling this
5:16
function with two strings and as a result what you would actually get here is probably an unwanted behavior because
5:23
if you add two strings javascript will concatenate the strings instead of doing
5:28
a mathematical calculation here so the result would not be five but 23 a
5:33
concatenated string of the two numbers this is an error you could have in JavaScript it's not a technical error
5:40
you probably won't get a runtime error but you have a logical mistake in your
5:46
code and that of course can lead to huge problems in the web applications you're
5:51
writing with JavaScript now of course in JavaScript we have mitigation strategies
5:56
we could add an if check in the function to check the types of the inputs at
6:01
runtime we could also validate and sanitize user input and whilst we might want to do all of that it would also be
6:09
nice if we could catch errors like this during development already and thankfully this is possible with
6:15
typescript because developers can write invalid code here in introduced box like this in JavaScript and with typescript
6:22
we have a tool that helps us write better and avoid such problems so let's have a
6:28
closer look at this here is this same example basically in a
6:36
real project you find this simple project the index.html file in this javascript file attached to this video
6:43
in a zip file you can simply open this and then open the index.html file you can also open the code in any text
6:50
editor of your choice here I'm using Visual Studio code and it will come back to my exact setup later
6:56
in this module for now you can just open these two text files with any text editor now what you'll find in there is
7:03
this JavaScript file which interacts with this index.html file and in that index.html file you'll find two inputs
7:11
and a button and any JavaScript file which gets imported here we basically reach out to these elements then we have
7:17
a function here and an event listener on the button that triggers the function and locks the result of the function
7:23
here in the console now if we simply open that index.html file by double
7:28
clicking on it in the Windows Explorer or the Mac finder so that it opens up in
7:33
a browser what you'll see is this the two inputs and the add button and here I
7:38
opened the browser developer tools as well now if you enter ten and five here
7:44
for example you might expect to see fifteen as a result here on the right but instead you see 105 and this shows
7:52
us a weakness of JavaScript here this is not a technical error it's not an error
7:58
which is thrown but it's a logical error in our application now where is this
8:03
error coming from though well here in JavaScript I reach out to these two
8:09
inputs and when the button is clicked in the end I get the values of the two input elements and a pastor here to add
8:16
and here it's important to know that in JavaScript when you access the value of
8:21
an input element it's always a string always no matter which type of input
8:26
disease if this is of type number or not it's always a string so I'm passing in
8:32
two strings to this function the end and if you add two strings in JavaScript they get concatenated instead of added
8:39
mathematically which is why we see one hundred and five ten and five concatenated this is the issue with
8:46
javascript here and this is something where typescript can help us now without typescript we could of course add a if
8:54
check here and check if the type of num1 is equal to number and if the type of
9:01
num2 is equal to number and if that is the case then I return my calculation
9:08
like this else I might throw an error or I at least convert both to numbers by
9:15
adding a plus in front of each parameter here now this is some code we could
9:21
write maybe a bit more refined than this in JavaScript and with that we would
9:26
ensure that we convert numbers or the inputs to numbers if they're not numbers yet so with that if I reload this and I
9:34
repeat this now we get 15 because of our changed code so of course you can do
9:39
this in JavaScript and this is vanilla JavaScript nothing typescript is about it but we wrote some extra code for an
9:47
error which I actually would like to prevent in the first place I don't want
9:52
that this happens I want to make sure that we can't even pass strings here to
9:57
add because add should be a function that only operates on numbers so that in
10:02
there we don't need to check whether we get a number or not so I want to keep this function in this state it was
10:09
before I want this function here just like this and that is where typescript
10:14
can help us so typescript can help us in such situations as I just showed now in
10:20
order to see how it helps us let's install it so on typescript Lang org you
10:26
can click on download' and there you'll learn how to install it and we will actually install it with
10:31
this command which uses the NPM tool and the NPM tool is part of the note Rhea's
10:36
package so even though we're not going to write no trayers code here we still
10:41
need to install node.js simply because behind the scenes that will also be used
10:47
by some tools we use and when we install node.js we also install NPM the node
10:53
package manager a tool which we then can use to install typescript globally on
10:58
our machine so simply visit note reyes org and there install the latest version you find here
11:05
simply click on this button it will then download an installer you can walk through that installer it is supported
11:11
for all operating systems and once you have noches installed you will be able
11:17
to run this command simply open up your normal terminal or command prompt and
11:23
then copy in that command important on Mac and Linux you might need to add sudo
11:29
in front of this to get the right permissions on Windows this will not be required so simply make sure you then
11:35
install typescript with this command enter your password in case you should be prompted for it and with that you got
11:42
typescript installed globally on your machine now what does this mean typescript
11:47
installed well remember that typescript is a programming language but it's only
11:52
a programming language that works because we also have this compiler this tool which compiles it to JavaScript so
12:00
in the end what we installed here is the compiler and everything it needs to know
12:05
to understand typescript code to convert it to JavaScript so with this we have
12:11
the compiler installed and we can run the TSC command now which invokes this
12:16
types of compiler to compile a types good file to JavaScript so to see this
12:22
in this project we worked on let's simply add a new file using TS dot ts
12:29
for example any name you want but the extension should be dot TS which stands
12:34
for typescript now let's copy that JavaScript code into that types could
12:40
file here in visual studio code I immediately get some errors which we now will fix and this is one great advantage
12:47
of typescript if you're using the right IDE and my strong recommendation really
12:52
is visuals to your code and I will come back to it later then you already get great support in the IDE when working
12:59
inside of typescript files here already it basically lets types could analyze my
13:05
code and identifies some weaknesses which is great because that's exactly what I want
13:10
so here in this example let me delete the jobs could only J's file and with death some of the
13:18
errors are gone because it identified that some constants and so on were used in multiple files but it still gives me
13:25
an error down there and what you see for example is that it's not sure if there really is a value property now that's a
13:32
mistake I didn't even consider before in JavaScript but it's true I'm selecting an element by ID here now
13:40
typescript can't know if this will really work maybe I have a typo in here in this case I wouldn't be able to
13:45
select an element this element simply wouldn't exist on the page so we might have a typo in typescript does not
13:51
analyze your HTML code to find out if this works so for one this might fail but even if it succeeds and we select an
13:58
element there it doesn't have to be an input element it could be any other element and most HTML elements don't
14:06
have a value property you can access and this already is great typescript forces
14:11
us to be more explicit to be clearer about our intentions and to double check our code and for example here and you
14:18
don't need to understand all that syntax we will learn it step by step throughout the course but for example here we could
14:25
let type know that we are sure that we will get an element by adding an exclamation mark this basically tells
14:32
typescript this will never yield null this will always find an element and as
14:37
a developer I of course know that this will always find an element because I double check that ID and I see yeah I
14:44
have that ID here now in addition I also know it will always be an input element
14:50
so we can use as HTML input element a syntax called typecasting which I will
14:56
also explain in greater detail later to let typescript know which type of element this will be we can apply this
15:02
to the second element as well so just to be really clear here this is typescript
15:08
syntax I can use this exclamation mark here and I can use this typecasting here because we are in a dot ts file we are
15:15
in a types could file we will compile this to JavaScript this would not work in vanilla JavaScript this is not
15:22
available there with this we are forced to be clearer about our intentions and to really think
15:29
about our code and double-check it which is great but that's not even the biggest advantage the biggest advantage is the
15:36
addition of types that is what gives typescript its name after all and here
15:42
I'm not saying anything about the types of data this function operates on if we
15:47
hover over one of these parameters we see this anything here and in the end this is typescript saying to us I don't
15:55
know what's in there it could be any type of value now we can add a more
16:00
explicit type in typescript files so not in JavaScript files but in typescript
16:05
files by adding a colon here and then specifying the type for example number
16:11
doing this here and doing this here with this extra syntax which typescript which
16:17
this compiler understands we're telling typescript that this year will be of
16:22
type number and this will be of type number and therefore now we get an error here again and we don't just get this error in the
16:29
IDE by the way we also get it if we try to compile this code because that is ultimately what we need to do right now
16:37
to compile this I will open a terminal and here I'm just opening my terminal or command prompt which is integrated into
16:44
this IDE it's the regular system command from the regular system terminal I was
16:49
using here as well just already navigated into this folder so if you are
16:55
not using some built-in IDE terminal you can use your regular one but CD navigate
17:02
into that extracted starting folder where you added your type script file and once you are in that folder you can
17:10
run TS c that will invoke this typescript compiler we installed earlier on using - TS TS and if you run this you
17:20
will actually get an error you will still get a JavaScript file because by
17:25
default typescript will still compile it to JavaScript you will also learn how to
17:31
suppress this later in the course but it gives you a compiler error while doing
17:37
so it tells you that argument of type string is not assignable to parameter of type number
17:43
so the problem here is that typescript understands that what we get on the
17:48
value property of our input element will be a string we also see this here in the
17:55
IDE and we can't pass this to add because there we don't want a string we
18:01
want a number so we have to fix this by for example converting this to a number here by adding a plus and as soon as we
18:08
do this we can compile this code again by repeating that command and now it
18:14
compiles without errors it gives us this using typescript our javascript file and now it shows some errors again because
18:22
it doesn't understand that I will never use both files at the same time here again this is also something which will
18:27
get better later in the course once we configure this we can ignore this for now so it gives me this file and if we
18:34
open this we see something interesting in here we see that there of course our
18:39
types are gone this casting here is gone we have vanilla JavaScript again so if
18:45
we have a look at our types code file here we see that there we have all these nice additions but as I mentioned these are
18:51
just types with features when you compile to JavaScript they are used to
18:57
evaluate your code and to find potential errors but then they are stripped out and we get regular JavaScript as output
19:04
so now we can go to our index.html file and import using T SJS and that's
19:11
important always import JavaScript files because the browser can't run typescript
19:17
we need to import the result of our compilation and now with that if we
19:22
reload this we have our working code because now we have proper JavaScript
19:28
code where we fixed this issue by casting our inputs before we pass them to the function but we were able to fix
19:35
these issues because of our type annotations here and as you saw we had
19:40
to write some other parts of the code in a cleaner way as well and dad is white typescript is amazing it forces us to
19:47
write better cleaner and less error-prone code
19:54
so you saw typescript in action and it offers great advantages it makes writing
20:01
clean code really easier typescript adds types and data is super important
20:07
with types we have to be way more explicit about how things work and we can avoid many unexpected and
20:14
unnecessary errors by using types in addition to that we also can use IDE s
20:20
modern IDE s which have built-in types of support which can pick up on these types and give us better order
20:27
completion and built-in errors which show before we even compile the code because they also understand typescript
20:35
but besides the types and the huge advantages we get alone by using types
20:40
we also get our features added by typescript we can use certain next-generation JavaScript features
20:47
which you can write and use in our typescript files and then they will get compiled down to JavaScript code to
20:55
workarounds that even work in older browsers if you know Babel which is a
21:00
tool that allows us to do that with vanilla JavaScript as well it's a bit like that just already built into
21:07
typescript we can use modern JavaScript features and still produce and ship code
21:12
that works in older browsers as well types could also add certain features
21:18
which only times could understands like interfaces and generics these are features which can't be compiled to
21:24
JavaScript but they don't have to because they are features that help us during development that give us clearer
21:31
errors and help us avoid even more errors so it even adds more features on
21:37
that front besides the types we already learn about it also gives us certain meta
21:42
programming features like decorators on which I have a whole module in this course where you will understand what
21:49
exactly decorators are why they are so meta and why they are amazing
21:54
typescript also is highly configurable we didn't configure it thus far but I
21:59
have a whole module in the course where we talk only about the compiler and how to configure it and you can really find
22:07
unit to your Harmons to make it stricter or looser and to ensure that it behaves in exactly
22:13
the way you want it to behave and with modern tooling with modern itës you even
22:20
get support in non types good projects the IDE you just saw Visual Studio code
22:26
that even gives you better support in plain JavaScript files because it is
22:31
able to use some types good features under the hood without you explicitly
22:36
using typescript so that's a free gain you get out of the box when being aware
22:41
of typescript and when using modern tools so there are many reasons for using typescript and that's probably why
22:49
you took this course in this course we will now learn it step by step and we will learn all about the amazing
22:55
features it adds
23:00
this course is packed with content we're almost done getting started and
23:06
thereafter we'll dive her right into typescript and into all its exciting features and learn them step by step
23:12
we'll start with the typescript basics of course the core types how it generally works some of the new features
23:19
it adds and all you need to know to get a good understanding of typescript thereafter will already dive deeper into
23:26
the typescript compiler and the configuration of it because it's super important for you to understand what you
23:33
can configure there and what all these different settings do is it will have a closer look at that in this module
23:39
thereafter we'll explore next-generation JavaScript features supported in
23:44
typescript how are they work and how you can use them in typescript will continue with classes and
23:49
interfaces a super important concept partly also in vanilla javascript in the
23:55
case of classes but with interfaces we also get a brand new typescript feature and you will understand what they are
24:01
what they do and why we might want to use them there after it's time to dive
24:06
deeper we'll have a look at some advanced types and advanced types good features in general taking it to the
24:13
next level there and building up on the basics we already learned about up to this point also an advanced feature
24:20
which definitely deserves its own section is the generics feature you will
24:26
learn what that is and why it's really really helpful in this module followed
24:32
by decorators decorators are a pretty cool feature also added by typescript
24:38
and we'll have a closer look at decorators and also build some really useful decorators in that module and
24:45
thereafter we will have learned a lot about typescript now the course is
24:50
organized such that I show all these individual features in relatively small
24:55
simple demos now to also give you a bigger picture and to see how you would
25:02
apply all these features in a real project we'll build just that we'll have a whole
25:07
module where we built an entire project entirely with typescript
25:13
from scratch so that you see many of these features most of these features you learned about up to that point in
25:20
action and you see how they work together and why they simplify the process of building such a project once
25:27
we're done building this project we'll identify a new problem and we'll learn how to solve it by working with
25:33
namespaces and modules which will help us make our code more manageable and readable building up on that we'll also
25:41
explore webpack with typescript webpack is a build tool we use in modern front-end web development and you can
25:48
use it combined with typescript to get a better project setup which simply make certain things easier and allows you to
25:55
get the best of both worlds a great development experience and all the code that works really well for your
26:01
end-users once we're done with that we have a very solid picture of typescript
26:07
and how to work with it in project now what you will need in a lot of real projects are third-party libraries so we
26:14
will take a closer look at that because there are certain third-party libraries which really embrace typescript and have
26:21
built in typescript support but there also are many libraries which don't and we'll have a look at how we can work
26:27
with both types of libraries in a great way in typescript project well and then
26:34
there are some specific scenarios which deserve their own modules we'll have a
26:39
whole module about react with typescript how you can build an entire react
26:44
application with typescript only and also an entire module about node.js and
26:50
Express and typescript so that you also have great examples for these very
26:55
popular and specific use cases of typescript where you can suddenly create
27:00
react or node applications in a brand-new way with a brand new language so lots of exciting content in the
27:07
course let's not waste any time let's see how you can get the most out of the course and thereafter let's dive in
27:18
your success matters to me and I want to ensure that you get the most out of this
27:23
course now of course that starts with watching the videos this is a video on the Monde course self course watch the
27:30
videos you can go through this course step by step it's built in such a way that all the modules and lectures build
27:37
up on each other you can also skip certain modules of course because all the modules all do work on their own if
27:44
you already know a concept for example now when watching the videos of course do that at your speed you got speed
27:51
controls here in the video player and you can slow me down if I'm going too fast or speed me up if I'm going too
27:57
slow for your taste I also recommend that you code along it's not a must-do
28:03
but you typically learn better if you write code on your own and you have to find and fix your own mistakes all the
28:10
pause and rewinds the videos for that because the videos are of course recorded in a way that also makes sense
28:17
to people who are not coding along so if you do you might need to pause occasionally try out the next steps on
28:24
your own or go back to an earlier point in a video to see how exactly I implemented something there and in
28:31
general practicing is important in this course we work on real projects and we
28:36
have many smaller demos and I can only encourage you that you sometimes pause
28:41
and try out the next steps on your own or that you deviate from what I do and try out your own things so definitely
28:48
also advance on your own of course only to a certain extent because if you haven't learned about a certain feature
28:54
it might be hard to implement it on your own but whenever possible whenever you feel like it definitely try out things
29:01
on your own now when you do that or when you just code along as well
29:07
you will also face some errors things don't always go as planned you introduced a mistake in your code and
29:14
you get an error now debug these errors and search on your own use the attached
29:20
code which you find attached to many lectures in the course always to the last lecture of each module so that you
29:26
can compare your code to mine and find out where it deviates but also if you get air
29:31
messages google them or use the search here on udemy to also search the Q&A section because chances are someone else
29:39
had a similar error and you can quickly fix it by looking at their solution now
29:44
of course if you're really stuck or if some concept is unclear you can also ask but also answer here in the Q&A section
29:52
I do my best to provide quick support there but also try to help others there
29:57
on your own because besides fixing your own errors if you also help others and
30:03
work with our students you get a lot out of this course as well so that's definitely all the recommendation I have
30:10
and with all these steps or all these building blocks you have everything you