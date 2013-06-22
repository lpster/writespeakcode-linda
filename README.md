Summary: This README hosts a compilation of my notes at the Write-Speak-Code conference (June 20th-22nd, 2013).

##Write-Speak-Code
@writespeakcode
#writespeakcode
http://www.writespeakcode.com/

##Notes from the Op-Ed Project
http://www.theopedproject.org/

What if you knew the cure for cancer? Would you speak up?
- Yes, if the situation is about other helping people

###RESOURCE vs. EXPERT
- Resource: being helpful and useful to somebody
- Expert: a term of power

The risk with not speaking up when you're feeling insecure about not being the "expert" on a topic is selfishness. 

> "Because I don't know everything, nobody gets to know what I know."

###When writing an op-ed...
- Envision the likely outcome and challenge people to take it on by the end of your column. 
Otherwise, it'd be difficult to achieve it. 
- You need an argument that is **timely**. News hooks could include breaking news/current events/births/deaths/anniversaries/releases of new data/trends. ALTERNATIVELY, you could hijack the news!
- Your argument needs to be **evidence-based** (e.g. studies, data, expert quotes, personal experience (which CAN BE superbly powerful -- think Angelina Jolie's op ed about getting a double masectomy)...
- Your argument needs to be **value-based (of public value)**
- Your **lede** needs to grab the reader's attention
- Include a "TO BE SURE" in your op ed. The "TO BE SURE" recognizes that counter viewpoints exist and recognizes them, but underlines the value of the author's point. It takes a perceived weakenss of the op ed's argument and turns it into a strength. For example:
<"To be sure, there are older and more experienced persons who have worked on education policy for several years... but when was the last time you heard about education reform from someone who just recently still had a locker combination?" -- From a recent college graduate writing about education reform
<"I know the movies are great, but the theater..."
- Remember the triangle of relevancy. That is, even if your master's thesis is on a specific topic in a specific period of time, you can expand along theme lines for your specific expertise. 

**How to Pitch**
Answer the following questions:
- So what?
- Why me?
- Why now?
- Aha! POV (what am I adding to the conversation?)
- Economy of words. Do not put drafts in attachments. 
- Mind the power of words -- use exactly the words that you mean. 

sheetaluk@spotify.com came to speak to us about working at Spotify, and gave us advice, such as:
- practice
- do not be self-critical in an interview
- don't be afraid to pursue a job posting because you "don't meet all the requirements." Many of them are optional.

=====
Public domain books include Jane Eyre, Huckleberry Finn, Pride and Prejudice, Dracula, The Picture of Dorian Gray, Wuthering Heights, etc. are examples of books that are in the public domain. They're free to take and make. 

*FreeBSD or MIT License* - this is the most popular one. "Do whatever you want but don't call me about it."

*GNU General Public License (GPL)* - "Everything must be open-sourced from here on out."

*Mozilla Public License (MPL)* - "You scratch my back, I'll scratch yours."

*Dual License* - If you're using it for open source, that's fine, but you have to keep it open. If you're using it for commercial use, then you have to pay. 

***Other Terms
*Copyleft* - a play on copyright -- means that the work is automatically open and must be shared. Derivatives welcome.
*Commercial* - Others can't make money on it
*Reciprocity* - Improvements must be shared

"Commercial" and "proprietary" are not the same thing. 

**The ThinkUp Project**
http://github.com/ginatrapani/thinkup

##Resources for finding open source projects
http://bit.ly/FindingOSSProjects

Reasons to work on open source projects:
- Scratch an itch
- Visibility
- Street cred
- Code to play with
- Help the community

###Open source contribution stories:
**Fureigh**
- The idea that "you must be this smart to contribute" is not true.
- The developers on the project were saying it's not possible to do XYZ. 
- There happened to be an informal Drupal camp going on the next week. Met someone (Angie) who later became a lead on the Drupal code.
- Started running a Drupal meetup in NYC. Helped people roll patches, use git, etc.
- At another DrupalCon, there was an in-person sprint of hundreds of people. Fixed a typo in the code -- and was recognized at the live code review session, and became a 'core contributor' to Drupal for a day. So, no matter how small...
**Leah**
- Now a contributor on the Julia programming language because of participation in Hacker School

**Serena**
- Code for America - got involved in an open source project in New Orleans

Fixing development setup documentation is really important and can be very helpful for a lot of people.

Places you can find projects:
- CodeMontage
- Open Hatch
- Code Triage
- 24 Pull Requests
- Git Rec


###Open Source Security - how to get lots of security for a low, low price
- Rachel Engel
Open source projects - are done by volunteers
SSL. Using HTTPS.
- Globalsign is offering free certificates for open source projects. 

**SQL Injection**
- On a technical level, SQL injection is a completely solveable problem if you plan well.
- Example of vulnerable code
< $string = "select*from table where field='"+$user_input+"';";executie_statement(string);
- If we separate the data from the query, the statement is no onger vulnerable. Enter parameterized queries.

**Cross Site Scripting (XSS)**
- It's best to think of XSS as HTML/Javascript injection
<$username = webservice_input();
$html = "<html>Hello, " + $name + "<html>";
- Before you output any data from your user, translate every ">" into &gt and "<" into &lt. 
- If you do it from the getgo, it's cheap.
- Session cookies: apply HTTP Only and Secure flags to your session cookies
- Input Validation: Don't accept > or & in anybody's name.

**Password Storage**
- Never try to roll your own password storage. It's really hard.
- First wrong answer: storing passwords in plaintext. If the database gets lost, lattackers have the users passwords trivially.
- Second wrong answer: just apply a hash. Hackers have multi-terrabyte tables mapping common passwords to their SH-1 and MD-5 hashes. You can download them from the web. 
- Hash functions don't often work because hackers have CD-ROMs of 30 million most common passwords that they can run hashed passwords against.
- If you make the hash function take a longer time instead of one millisecond, the user isn't going to notice when they type in their password, but the function will take a longer time to run. Use a per-password salt, and make the hashing process really slow.
- The attackers need the hashing to be quick in order to attempt aenough passwords for successful brute forcing.
- **Bccyprt** -- a hash algorithm designed to be tunably slow. You can say how many times you want it to run the algorithm when hashing with it.
- Implementation for Java, Python, C, C#, Ruby, Perl, PHP


**Cross Site Request Forgery**
rachel@isecpartners.com - Rachel Engel

There are so many bugs. Developers often don't have time to keep track of every security bug.

Are there any groups specific to people interested in security?
- If you were in to open source 
-owasp.org
-burp proxy - http://portswigger.net/burp/proxy.html

How do you report security bugs to the community?
- If you start looking for SQL injection bugs on other people's websites you're breaking the law. There are people who have reported bugs and then gotten prosecuted.
- Only test out bugs on software you write yourself.
- Microsoft and Google will pay you, but other big companies will sue you.

###Feminism and Open Source
Corey Latislaw @corey_latislaw
Pam Selle @pamasaur , thewebivore.com, front-end developer at Paperless Post

High-level view of feminism: A lot of women don't have any background in understanding feminist theory.

NEW MODEL: 
- Warmth
- Mentorship -- e.g. sprints, hackathons, sprints at PyCon
- Stewardship: answering questions and being accessible to new and regular contributors
- Open Discourse - clear communication

© Copyleft
