java c
Assignment – Spatial Data and Asset / Facilities Management 
Submission Date: see Moodle, note pre-submission topic declaration 
Submission Method (links to all forms on Moodle): 
o Pre-Submission – 
Declare your topic title, description and the names, geometry types and dimensions of your three location-based, nested, assets 
– to avoid risks of plagiarism your topic area should come from the existing list.    Online form, first come first served 
o Submission 
A PDF of your pyramid, uploaded via Moodle / Turnitin 
Completing an online form. with information about the decisions you are making 
Five separate SQL scripts via an online form 
A PDF of your map uploaded via Moodle/Turnitin 
A PDF of your 3D visualisation uploaded via Moodle/Turnitin 
This assignment is worth 70% of the marks for the module. 
- An assignment is an independent piece of work: 
o Your work should not be identical to, or similar to, that of any other 
student or the work we do in class. Please make sure you follow all UCL procedures for academic integrity. 
o Discussing your assignment work or sharing your work with other students or having very similar answers is collusion. 
- If you have questions about this assignment, please post them on Moodle 
- That way everyone is given the same information 
- That way I remember what I’ve said to you and don’t mark you down for doing something that I wasn’t expecting 
- Any questions should be generic – as this is an assessment which will gauge how much you’ve learned during the module I won’t be able to solve very specific assignment-related problems for you. 
- Do not post any part of your assignment answer on Moodle 
- We reserve the right to block the Moodle forum if too many questions are 
asked multiple times and/or if questions are asked where the answer is in the assignment text.    This would mean that none of your fellow students will be able to ask questions so be very careful! 
-  The deadline for posting questions is 5 days before the assignment deadline 
- This is a digital submission – it is up to you to ensure that the files you upload to Turnitin or the online submission process are not corrupt in any way (in Turnitin 
you might be able to do this by downloading the uploaded files to check them, for the online submissions you will receive an e-mail which you should keep as 
evidence of successful submission) 
NB: You are limited to a maximum of 10 e-mails per day to avoid overloading the testing system
Database Design and Build (70%) 
Overview The assignment involves   the selection of a location-based asset management topic of   your choice for which you will create   a   hierarchical   pyramid   to show   how   the   features   (assets) and decisions based on information about those   features   nest   upwards.
The pyramid should have 3 levels of spatial nesting You   will   then   make   a   list   of   7 decisions.   Two   of   the   decisions   MUST   use   data   output   from   lower   level   decisions   (i.e.   bottom->   middle   and   middle   ->   top).       All   decisions   should relate to ONE level of the pyramid (up to   you which level for the other decisions).
You   will    then    create    the    physical    database      for    your    topic,    insert    some    data    and   demonstrate using queries   how this data can   be   used as evidence for the decisions.
Step 1 - Topic Pre-Selection/Declaration (online form, link on Moodle) 
See Moodle for details of where the topic   list   has   been   sourced   from.
You MUST check the topic description before you select a topic, and make sure you understand the topic. If the remainder of your assignment does not match the topic you will not pass.Select a topic and provide a topic title and   list your three   spatial   asset   tablenames   and   geometry types and dimensions.       These must be nested   (i.e. the top   level contains the   middle   level and the middle   level contains   the   bottom   level):
•         The top   level should   be a   3D volume
•         The   middle   level   should   be   a   3D   volume   or   a   2D   area   (provided   it   nests   inside the top   level   using st_contains)
•         The bottom level can be a 2D or 3D point   or a 2D   or   3D   line   or   a   2D or   area   or a 3D   volume (provided it nests inside the middle level using st_contains)
Not   nesting the assets correctly will   result   in marks   being   lost for   decisions   as   well
There is no specific deadline for this task but you should make sure you lock in your topic BEFORE doing any other work on the assignment! 
You should not use a university or school example as this would be too similar to the example we covered in class and would be plagiarism. Your decisions should also not be similar to those used in the class or lab examples – i.e. do not adapt existing text and SQL – make sure you start completely from scratch.
Step 2 - Decisions (online form, link from Moodle) 
List the Decisions (link to online form. will be given in Moodle) 
1.    Write a description of the 7 decisions that   your   database   will   support
• The decisions need context and   should   include   some   information   as   to    what    information    is    needed    but    also WHY    the    information is needed, how it will be used by the decision maker - In   other   words,   you need to be clear on what the information will   actually   be   used   for
- what is   being   decided.
•         All decisions should be   based   on   a   numeric value
•          Decisions should also include a   realistic threshold value   in the   text
See Appendix and Step 4 for further information.
2.    You   should   have   two   decisions   that   build   on   information   provided   by   a   lower   level   query   (i.e.   three   decisions   in   total)   .      You   should   make   use   of   VIEWS   to   achieve this.
•         Create   a   view   for   the   decision   corresponding   to   the   bottom   level   of   the pyramid, and for the   decision   query   select   from   this view
•         Create a view for the   decision corresponding to the middle level of the   pyramid that includes data from the view from the bottom level of the   pyramid, and for the decision   query   select   from   this view
•         Create   a   view   for   the   decision   corresponding   to   the   top   level   of   the   pyramid,   that   includes   data   from   the   middle   level   view,   and   for代 写Assignment – Spatial Data and Asset / Facilities Management
代做程序编程语言   the   decision query select from   this view
Step 3 - Pyramid (turnitin upload) 
1.    Create a THREE LEVEL pyramid for this organisation - similar to the example from   the Centennial case study. This should include the names of the spatial   asset/features that are at the bottom,   middle   and   top   levels   of your   pyramid
a.    These names must be IDENTICAL to the   name of the   table   that stores   data   for this   feature.
b.   All table   names should   be   lower case
c.    All   three   tables   (assets)   must   match   the   tables you   declared   in   the   pre-   submission stage
d.   All   three   features   must   be   spatial   -   i.e.   mappable   (they   can   be   2D   or   3D   depending on how they were originally   declared)
e.    The    features    must    nest    -      i.e.      features      at      the      lowest      level      must      be   contained inside features at the   middle   level, and   features   at   the   middle   level contained inside features at the   upper   level.
Include   a   cover   sheet   in   this    PDF   as   Moodle    requires   a    minimum   of   35   words   for   plagiarism checks.
Step 4 - Database creation (5 script. files, online form) 
For this part   of   the   assignment:
1.    Script. creation   as   follows:
a.    Create an SQL script   that   contains   the   SQL   used   to   create   the   tables   in your   database system.    Call this script. createtable_ucxxxxx.txt   (where   ucxxxxx   is your UCL login). All table names should   be   lowercase,   use _ to separate   out any words   (not spaces   or   -)
• Make   sure you   use   addGeometryColumn   to   add   location   columns   –   the SQL testing scripts will   not work if   this   is   not   present
• Make sure you use the parameters approach following   the   in-class   example.
b.    Create    a    separate    SQL    script      for      all      the      constraints.             Call      this    script.
createconstraints_ucxxxxx.txt 
c.    Create a separate SQL script. to populate each table   with data - call this script. insertdata_ucxxxxx.txt:
• A   minimum of 2   rows of data for   the   top   level of   the   pyramid
• A   minimum   of   3   rows   of   data   for   the   middle   level   (nested   within   the   top   level data)
• A   minimum of 9   rows of   data   for   the   bottom   level   (nested within   the
3   rows of the   middle   level)
• A   minimum of THREE rows of data   for   all   other   tables.
The data should be sufficient to allow you to test out the SQL for your   listed decisions.So   that   we   can   test   your   work   independently,   your   SQL   must   create   ALL the data required from scratch – don’t use any   data   that   has   been   imported via QGIS   / sourced from third   parties.      The   spatial   data you   create   does   not   need   to   be   very   sophisticated   in   terms   of   geometry   complexity.All data should use a projected coordinate system (i.e. not lat/lng –    if you    don’t    know    the    projected    coordinate    system    for your location use British National Grid) 
d.    Upload   a   script   that   creates   a   series   of views   that   will   help   to   simplify your   queries   –   minimally,   you   should   have   3   views,   one   for   each   level   of   the   pyramid   that   aggregates   from   the   lower   levels. You should also have a latest_parameters view. Your file should only contain views – do not include   the   select   statements   to   test   the   views. Call   this createviews_ucxxxxx.txt
e.    Create a script. file with the   7   SQL   queries   that   provide   data   used   to   support   the    decisions    you      listed    in      the      first      part      of      the      assignment.      Call      this
decisions_ucxxxxx.txt 
•         The   result   of   each   decision   query   should   appear   as   a   three-column   table, with ONLY ONE   ROW as   follows.:
Decision 
Threshold Value 
Result 



• The decision text is hard coded in your SQL, the threshold value is hard coded in the SQL, the result is a number calculated from the 
inserted data. 
As a very simple example of hard coding in SQL (note the single straight   quotes)
select ′This is a decision ′, ′22.3′,    << your result SQL goes here>> from ucfscde.buildings; 
• To meet the Step 2 (2) criteria, three of the seven statements should be just
select * from ucxxxxx.view_name 
2.      Use the provided test system   (link on Moodle) to   upload   and   test   your   scripts.   You   will   receive an e-mail   report each time you run   the   test.   Keep   this   as evidence that you have submitted your   scripts.
Some CHECKS 
•          The SQL scripts should be   manually created   –   i.e.   typed   by you
•          You must use   the   provided   PostGIS database
•          The   first   line   of   the   createtable   script   should   drop   cascade   the   ucxxxxx   schema   (if   it   exists) and create   it   again
•          All the SQL should work in your schema – e.g. your create table scripts should be similar   to: create          table ucxxxxx.buildings          (……), your         insert         scripts insert          into ucxxxxx.buildings and queries select from ucxxxxx.buildings 
•          Do   not include views in the decision   queries   –   use   a   separate views   file
•          Include    comments   in   your   scripts   to   make   them   easy   to   read   –   use    --   to   mark   the   comments
o   Any comments should be   prefixed   by   --         (not   /*    */)
•          Each   element   (create   table,   constraint,   row   insert,   decision   query   etc)   in   the   script   should   be separated   by a   ;
•          Make sure that the filenames   are   correct.
• Any    decision that    requires    the    use    of    number values    as    part    of the calculation -   distances, minimum or maximum sensor   values, cost for painting, available budget and similar should use parameters.
Step 5 - Map and 3D visualisation (one PDF via Turnitin) Upload a PDF to Moodle containing a QGIS screenshot showing the spatial data you   create and a 3D screenshot created in FME. The screenshots should include the   entire QGIS/FME windows (including menus and layer list) so that it clearly   shows   that the data is spatial and the map has been created from data in the database.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
