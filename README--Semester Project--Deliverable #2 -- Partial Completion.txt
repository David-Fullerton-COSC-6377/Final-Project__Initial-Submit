(05-07-2015 Thu @9.07 am)

David Fullerton
Semester Project:  Deliverable #2
COSC 6377:  Networking class
Spring 2015
***************************************************************************

                  -----------------------------
                  OVERVIEW OF THE DELIVERABLES:
                  -----------------------------

[As an initial note, I am submitting it partial with most of the
framework there to show that I care about this class and project.
Having been busy this semester and hardly any long-term breaks
where I can focus on something this detailed, I plan to keep 
working on it today until I get everything completed.  But, I will
go ahead and turn-it in where I can show that I respect deadlines.]

This is the second deliverable for the semester project.  This code
base is designed to hit the deliverable/s that were set-up for 
being achieved by this milestone.  And, the desired results are
achieved by this version of code.

This is a readme to explain real quick what is happening in this lab.
There are two different programs:  Client.c and Server.c.  They are
written in C (not C++) and are large files that have similar code.
But, the initial slice of the project is an end-user based application 
that is called the "Client.c".  The client is set up to be the 
communicator and interactor with the end-user.  It will act like a 
menu-driven application.  However, the other side of the project
is the server-like application called "Server.c".

The two different applications communicate and work together to 
achieve the second list of milestones for the semester project.  
The Server is designed to count the packets that are coming from 
the Client, and I added the feature of the Server counting the number 
of characters transmitted also.  Therefore, the Client will send
a particular number of characters per packet (a variable that
can be changed), and the Client will allow the user to pick a
length of time in seconds that the Client and Server will run 
until the Client tells the Server to stop counting.  Also, the
Server has another variable called "Max Packets Per Second" that
can be set to only allow so many packets to be sent in a single
minute.  This variable helps show that the speed of transfer
can increase and/or decrease.

After the specified time has elapsed, the Client will tell the
Server to stop, and the Client will end its program.  Whereas,
the Server will show a visual tally on the screen of the performance
for each second during the last run.  This will provide the
number of packets received and the number of characters that
were able to be transferred during that time period.

The final project was to have a webpage run that shows a page
with a "+" button and a "-" button.  The PLUS button would 
speed up the Server application and make it send more packets,
whereas the MINUS button would slow down the Server application
and how many packets it is sending per minute.  The speed of
the packets can be increased by copying and renaming the 
"n-increase.inf" to a "n" file for increasing the speed of the 
packets being sent as the Client is running.  Similarly, the 
speed of the packets can be decreased by copying and renaming the 
"n-decrease.inf" to a "n" file for decreasing the speed of the 
packets being sent as the Client is running.  In the current
implementation, it will always decrease by 1000, but this 
was to be an amount that would be on the webpage.  Therefore,
it still needs to be implemented.

Next, I have not yet worked out the details of the SMTP 
implementation.  I understand that it needed to send mail, and
I would have loved to get that going.  But, I plan to keep going.
Also, I did practice installing Apache on the AMI instance, yet
I have not also practiced it on my local Linux machine.  So, I
plan to also practice getting that installed too.  But, I did
prove that I could (after a lengthy time of working with
installation problems) get it going on the AMI instance.

So, the basic functionality is there.  It just needs a few of
the final "bells and whistles" that time this semester has prevented
so far.

***************************************************************************

                    ***************************
                    * COMPILING AND RUNNING : *
                    ***************************
                   
To compile these, I have created a quick compiler file called
"mc" which is a batch file to compile both applications.  First,
you must type, "chmod 700 mc", to change the properties of the
Make-Compile file where it will run on your system.  Then, if you
run it with "./mc" and don't see any errors, then the two programs
compiled without issue.  Before I sent them, they compiled without
issue/s.

Then, to run these applications, you need to type "./svr" to run
the Server first.  Then, you type "./cli" to run the client.  And,
the Client is where you will interact with the program and run
the tests.

There are four options in the Client.  Option #1:  This will show
you the current values of the default configuration variables, such
as:  (a) Number of seconds to run (default at 30), (b) Number of 
characters to send per packet (default at less than 50), and 
(c) Max Number of Packets per Second (less than 5000).  Option #2:  
Allows you to change the two configuration variables (see Option #1).  
Option #3:  Run the given test.  Or, Option #4:  Stop the program and 
end the testing.

Therefore, the above is a good overview of how the files in the
directory work.  I hope you enjoy testing the application and 
watching it give estimates of the performance between the Server
and Client applications that I have developed.

Thank you, DBF.

***************************************************************************

                   *****************************
                   * COMMENTARY (AS AN ASIDE): *
                   *****************************
                     
Also, I want to put it into print that I am not a "Last Minute" person.
Yes, it might seem that way this semester, but that is not the truth
of who I really am.  However, being a GTA, has put me behind the 
Eight-Ball throughout the whole semester, and I can not wait for a break.

Again, I am rushing to meet the deadline because I have other work
that (almost always) has to take priority.  So, I have not had it
like that many times in the past, but this semester is the first
semester that it has really been like that.

