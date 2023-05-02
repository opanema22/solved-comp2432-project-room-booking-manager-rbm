Download Link: https://assignmentchef.com/product/solved-comp2432-project-room-booking-manager-rbm
<br>
Project title: <strong>R</strong>oom <strong>B</strong>ooking<strong> M</strong>anage<strong>r</strong> (<strong>RBM</strong>)

PolySME Business Center is a company, which supports the concept of shared offices and provides office facilities to small business companies, especially those one-man companies.  The company offers general office facilities such as telephone lines, fax lines, LAN/Wi-Fi network, meeting rooms, etc.  PolySME finds that there is a problem with its current meeting room booking system designed 10 years ago.  It is not flexible enough to make good utilization of the meeting rooms and to satisfy most requests from its tenants.  In PolySME, there are three meeting rooms in use currently.  The three rooms are in different sizes; two are small, allowing 10 persons (<em>at most</em>) and the third one is the largest, capable of holding 20 persons (<em>at most)</em> in a meeting.  In addition, PolySME provides add-on/special facilities for each meeting room, for example, projector + screen for presentation/meeting use, or webcam + monitors for online conferences or meetings, to be set up in the rooms on demand.  Furthermore, such additional facilities come with different configurations.  For example, different projects/webcams support different resolutions, and the screens may be in different sizes.  Currently, tenants of PolySME may simply make a booking of a meeting room or book a room equipped with special facilities or reserve only the meeting facilities.  For example, Tenant_A makes a booking for a meeting room for 8 persons with a projector projector_2K with a screen screen_100.  If there are both the availabilities of the room and the required facilities, the booking request is accepted.  Otherwise, the booking request is simply rejected.  For instance, all the projectors of type projector_2K might have been booked by other tenants so that the request is rejected.  In the other words, that means the current system does not provide any alternative plan to satisfy or reschedule the booking when some of the requested item or location is not available for the requested time slot.

Knowing that you have learnt different scheduling methods from Operating Systems, the manager in PolySME is offering you a part-time job that you could use to satisfy your WIE.  Would you mind to help PolySME to revise its room booking system to achieve a better utilization with an improved scheduling/rescheduling method?  The goal is to improve the booking situation so as to increase company’s revenue on renting these to its tenants.

<h1>Project Requirements</h1>

In this project, you will be given an opportunity to apply the theory of process scheduling you have learnt from COMP2432 to a daily-life scenario and produce the <strong>Room Booking Manager</strong> (<strong>RBM</strong>).  The project consists of the following parts:

<em>Part 1</em>. Develop a program that allows users to add details of a booking (<em>date, time, duration, and/or callees etc.</em>) to the schedule.  Besides the standard line by line input approach, RBM should be able to read in batch files which containing the

booking requests, <em>i.e. one or more than one booking requests are stored in such batch files</em>.

<table width="614">

 <tbody>

  <tr>

   <td width="60"> </td>

   <td width="554">Note that the one who initiates for the booking is called the “<em>user</em>” or the “<em>caller</em>” and those others involved in the booking are called “<em>callees</em>”.  This part of the program module is referred to as the <strong>Input Module</strong>. <em> </em></td>

  </tr>

  <tr>

   <td width="60"><em>Part 2</em>.</td>

   <td width="554">Extend the program developed in <em>Part 1</em> with a scheduler to generate timetables for all bookings (e.g. meeting room booking schedule and tenant booking records).  The scheduler will implement several scheduling algorithms similar to those covered in lectures.  This is the called the <strong>Scheduling Kernel</strong>, within the <strong>Scheduling Module</strong>.</td>

  </tr>

  <tr>

   <td width="60"><em>Part 3</em>.</td>

   <td width="554">Augment the program with the facilities to print booking schedule for meeting rooms and related devices in <em>Part 2</em>.  Those rejected bookings should all be included.  This constitutes the <strong>Output Module</strong>.</td>

  </tr>

  <tr>

   <td width="60"><em>Part 4</em>.</td>

   <td width="554">Provide the program with the ability to generate a summary report to analyze the results produced in <em>Part 3</em>.  Compare the different schedules (<em>generated from different algorithms</em>) and find out which one would make the best use of the three meeting rooms.  Your program should preferably be able to process <em>N</em> meeting rooms (<em>N</em> = 3 in the existing case) to cope with the expansion of PolySME in the near future.  It should also be preferably able to handle more resource types in future. By the way, an outstanding (<em>rejected</em>) list may also be included in this report for those requests that cannot be scheduled.  This final module is the <strong>Analyzer Module</strong>.  <em> </em></td>

  </tr>

  <tr>

   <td width="60"><em>Part 5</em>.</td>

   <td width="554">Augment the program RBM to check whether or not the required facilities are available.  If so, it assigns a priority on each booking.  For example, if a room is booked for a presentation and should be equipped with projector and screen, the projector and screen will be reserved for that booking with a higher priority.  Even though the projector and screen have been reserved for another booking but without using a meeting room, i.e. someone reserves only the two pieces of equipment by that moment, the booking would be then rejected.  Of course, you may have other assumptions on how the conflicting bookings are being scheduled/rescheduled, and the associated priority.</td>

  </tr>

 </tbody>

</table>

You must form a group of 4 persons (<em>at most</em>) for the project.  The project must be implemented using the <strong>C programming</strong> <strong>language</strong> and it must be successfully executed on <strong>ANY ONE of the Linux Servers</strong> (<em>apollo or apollo2</em>) in the Department of Computing.  You may specify to us on which Linux server your project has been executed successfully.




<table width="606">

 <tbody>

  <tr>

   <td width="62">*****</td>

   <td width="544"><em>Note that we use only the “gcc” compiler to compile your program.  In other words, if your program cannot be compiled by the “gcc” of department’s servers, apollo or apollo2, we simply treat this as a failed program.</em></td>

  </tr>

 </tbody>

</table>

<h1>Implementation</h1>

<h2>User Interface</h2>

First of all, your program should provide an interface to allow the user to input the details of bookings and/or commands for the application.  There are several input methods to be accepted by the system, and the system should be able to store all requests (<em>valid and invalid</em>).

Below is an example of some inputs and outputs on a screen for reference.

<strong>Command Syntax and Usage</strong>

<table width="617">

 <tbody>

  <tr>

   <td colspan="2" width="617"><strong>To execute the program</strong></td>

  </tr>

  <tr>

   <td width="99">Syntax</td>

   <td width="517"><strong>./RBM </strong></td>

  </tr>

  <tr>

   <td width="99">Use</td>

   <td width="517">Simply to enter <strong><sub>[./RBM</sub></strong>] to start the program.</td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>addMeeting</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>addMeeting -aaa YYYY-MM-DD hh:mm n.n p bbb ccc; </strong><strong>e.g. addMeeting –tenant_A 2021-05-16 10:00 3.0 9 projector_2K screen_100; </strong></td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">It is to add a booking for a meeting room with certain devices together.  As in the example, [<strong>tenant_A</strong>] is to make a booking on [<strong>May 16, 2021</strong>] at [<strong><sub>10:00</sub></strong>], and the duration is [<strong><sub>3.0</sub></strong>] hours.  In addition, it also requires a projector (<strong>projector_2K</strong>) and a screen (<strong>screen_100</strong>).  [<strong><sub>-aaa</sub></strong>] – Tenant who makes the request.[<strong>YYYY-MM-DD hh:mm</strong>] – Date and time of the event, <strong>YYYY</strong>:Year (4 digits), <strong>MM</strong>:Month (2 digits), <strong><sub>DD</sub></strong>:Day (2 digits), <strong><sub>hh</sub></strong>:Hour (2 digits) and <strong><sub>mm</sub></strong>:Minute (2 digits).[<strong><sub>n.n</sub></strong>] – Duration of the appointment in hours (<em>one decimal place</em>)[<strong><sub>p</sub></strong>] – Number of persons to participate (<em>integer</em>)[<strong><sub>bbb</sub></strong>] and [<strong><sub>ccc</sub></strong>] – Additional devices to be required.  (<em>Optional, but should be in pair when request, [projector]+[screen] or [webcam]+[monitor]</em>) <strong>;</strong> – End of current input.<em>Note</em>: RBM would assign a room which fits the requirements.  For instance, RBM would assign either [<strong>room_A</strong>] or [<strong>room_B</strong>] since both are big enough to hold the 9 participants.  Of course, RBM would also check the availability of the required devices (<em>projector and screen</em>).  If all these are available, the request would be accepted.<em>          </em>For [<strong><sub>addMeeting</sub></strong>], it is an optional choice to book any add-on facilities.  Tenants may simply book a meeting room only.</td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>addPresentation</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>addPresentation -aaa YYYY-MM-DD hh:mm n.n p bbb ccc; </strong><strong>e.g. addPresentation –tenant_B 2021-05-14 08:00 3.0 12 projector_4K screen_150;</strong></td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">Similar to [<strong><sub>addMeeting</sub></strong>], it is to make a booking for a presentation.  As in the example, it is to add a request made by [<strong><sub>tenant_B</sub></strong>] who would conduct a presentation on <strong>[May 14, 2021]</strong> at <strong>[08:00]</strong> for <strong>[3.0]</strong> hours long.  And, there would be 12 persons to take part in the presentation.  In addition, the room should be equipped with [<strong>project_4K</strong>] and [<strong>screen_150</strong>].[<strong><sub>bbb</sub></strong>] and [<strong><sub>ccc</sub></strong>] – Additional devices are required (<em>mandatorily include</em>). The use of parameters is same as the previous one.</td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>addConference</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>addConference -aaa YYYY-MM-DD hh:mm n.n bbb ccc ddd; e.g. addConference –tenant_E 2021-05-16 14:00 2.0 15 webcam_UHD monitor_75; </strong> </td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">It is same as [<strong><sub>addPresentation</sub></strong>] but it would have a higher priority if you are to use the algorithm “priority”.  As in the example, [<strong><sub>tenant_E</sub></strong>] is to add a booking for a conference on <strong>[May 16, 2021]</strong> at <strong>[14:00]</strong> for <strong>[2.0]</strong> hours long.  The room should be equipped with [<strong>webcab_</strong><strong><sub>UHD</sub></strong>] and[<strong>monitor_75</strong>]. The use of parameters is same as the previous one. </td>

  </tr>

 </tbody>

</table>







<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>bookDevice</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>bookDevice -aaa YYYY-MM-DD hh:mm n.n bbb </strong><strong>e.g. bookDevice –tenant_C 2021-05-011 13:00 4.0 projector_4K; </strong> </td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">It is simply to reserve a specific device only.  As in the example, it is to reserve for <strong>[projector_4K]</strong> on <strong>[May 11, 2021]</strong> at <strong>[13:00]</strong> for <strong>[4.0]</strong> hours long.  That request is made by [<strong>tenant_</strong><strong><sub>C</sub></strong>]. </td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>addBatch</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>addBatch -xxxxx </strong><strong>e.g. addBatch –batch001.dat </strong> </td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">It is to read in a batch file, <strong><sub>batch001.dat</sub></strong> which is a plain text document and records one or more booking requests. </td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>printBookings</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>printBookings –xxx –[fcfs/prio/opti/ALL] </strong><strong>e.g. printBookings –fcfs </strong> </td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">It is to print the schedule (<em>Accepted and Rejected</em>) for users.  In addition, a“Performance Report” is needed if [ALL] is used.  The Performance Report is a summary of how many bookings are received and allocated, and how many are rejected in total that based on the algorithm used. Where<strong>–[fcfs/prio/opti/ALL]</strong> – Algorithms that would be used (<em>just a reference</em>).[<strong>fcfs</strong><sub>]</sub> – First Come First Served[<strong>prio</strong>] – Priority[<strong>opti</strong>] – Optimized[<strong><sub>ALL</sub></strong><sub>]</sub> – All algorithms being used in the application and the performance</td>

  </tr>

  <tr>

   <td width="100"> </td>

   <td width="517">summary report. In the example, the “First Come First Served” is used.  That is the first booking would be allocated to a time slot that other late requests which request the same time slot would just be rejected.For “Priority”, where the one has a higher priority rank can take over the time slot (see <strong>assumptions</strong> below).  That is, for example, a “conference” can replace an occupied time slot which has been assigned to a “Meeting”. For “Optimized”, actually there are different methods to produce an <em>optimized</em> result.  Here, in a simple word, it is to reschedule those rejected appointments.Then, there would be a better performance to utilize the facilities in PolySME.  In the other word, this part would be considered as the “<em>bonus</em>”. </td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="100">Command</td>

   <td width="517"><strong>endProgram</strong></td>

  </tr>

  <tr>

   <td width="100">Syntax</td>

   <td width="517"><strong>endProgram; </strong> </td>

  </tr>

  <tr>

   <td width="100">Use</td>

   <td width="517">This simply ends the program completely, upon collecting all the <strong><sub>child </sub></strong>processes and closing all the files. </td>

  </tr>

 </tbody>

</table>







To ease your work, we make the following <strong>assumptions</strong>:

<ol>

 <li>Input formats follow the examples and make no difference and we simply assume all the input formats are correct.</li>

 <li>Components in RBM are limited to the following:

  <ul>

   <li>five tenants – <strong>tenant_A</strong>, <strong>tenant_B</strong>, <strong>tenant_C</strong>, <strong>tenant_D</strong> and <strong>tenant_E</strong>;</li>

   <li>three meeting rooms – <strong>room_A</strong><strong><sub>, room_B</sub></strong> and <strong>room_</strong><strong><sub>C</sub></strong> (<em>room_A and room_B are of the small meeting rooms (&lt;=10) while room_C (&lt;=20) is the largest one</em>);</li>

   <li>three webcams – <strong>webcam_FHD</strong> × 2 and <strong>webcam_UHD </strong>× 1;</li>

   <li>three monitors – <strong>monitor_50</strong> × 2 and <strong>monitor_75</strong> × 1;</li>

   <li>three projectors – <strong>projector_2K </strong>× 2 and <strong>projector_4K </strong>× 1; Ø three projection screens – <strong>screen_100</strong> × 2 and <strong>screen_150</strong> × 1.</li>

  </ul></li>

</ol>

All these could be represented by [<strong><sub>child</sub></strong>] processes.  The parent process represents the PolySME to host all the bookings and can use different algorithms to <em>schedule/reschedule</em> bookings.

<ol start="3">

 <li>If a “<em>priority</em>” algorithm is applied in the booking system, you may consider that a “<em>Conference</em>” has the highest priority because it contributes the most profit. Then, it is “<em>Presentation</em>”.  The third one is “<em>Meeting</em>”.  Lastly, it is “<em>Device</em>”.  In other words, a “<em>Presentation</em>” may “<em>displace</em>” an already scheduled “<em>Meeting</em>” so that the caller/callee(s) involved would attend the “<em>Presentation</em>” but the “<em>Meeting</em>” would be <strong>canceled</strong>.  That could turn a previous “<strong>Accepted</strong>” status (<em>as the Meeting is successfully scheduled early on</em>) to a “<strong>Rejected</strong>” one (<em>overtaken by this more important “Presentation” event</em>).</li>

 <li>There are many implementation methods for the modules. The scheduler module may be implemented as a separate process, in the form of a child process created by the parent via <strong><sub>fork()</sub></strong> system call.  The output module can also be a separate process.  The scheduler may also be implemented as a separate program.  If the parent is passing appointment details to a child scheduler, one should use the <strong><sub>pipe()</sub></strong> and associated <strong><sub>write()</sub></strong>/<strong><sub>read()</sub></strong> system calls.  If the parent is passing information to a separate scheduler program, one could use the Unix shell “<strong>pipe</strong>” (denoted by “<strong>|</strong>”).</li>

 <li>If <strong><sub>pipe()</sub></strong> and <strong><sub>fork()</sub></strong> system calls are both used properly in the program and also the re-scheduling method/algorithm, the maximum possible mark is 100% plus up to 10% of bonus points. On the other hand, if both system calls are not used in the program, only a passing mark would be awarded.  Intermediate scoring will be given if only one type of system call is used, depending on the extent of usage.</li>

 <li>We test the schedule for a period, from <em>10 to 16 May, 2021</em>. One time slot is an hour of time.  That means each room should have 24 time slots a day and there are 7 days to be filled in.  You are recommended to overflow the time slots in the tests.</li>

</ol>

<strong> </strong>

<h2>Output Format</h2>

The “appointment schedule” – “ACCEPTED” and “REJECTED” may look like the following.

<table width="617">

 <tbody>

  <tr>

   <td width="617"> <strong>*** Room Booking – ACCEPTED / FCFS *** </strong><strong> </strong><strong>Tenant_A has the following bookings: </strong><strong> </strong><strong>Date         Start   End     Type          Room       Device </strong><strong>=========================================================================== </strong><strong>2021-05-10   09:00   15:00   Meeting       room_A     * </strong><strong>2021-05-12   12:00   16:00   Presentation  room_B     projector_2K                                                       screen_100 2021-05-15   09:00   12:00   Conference    room_C     webcam_UHD                                                       monitor_75 </strong><strong>… </strong><strong>… </strong><strong>Tenant_B has the following bookings: </strong><strong> </strong><strong>Date         Start   End     Type          Room       Device </strong><strong>=========================================================================== </strong><strong>2021-05-14   08:00   11:00   Presentation  room_B     projector_4K                                                       screen_150 2021-05-15   12:00   16:00   Presentation  room_A     projector_2K                                                       screen_100 2021-05-15   13:00   15:00   *             *          projector_2K 2021-05-16   10:00   15:00   Conference    room_C     webcam_UHD                                                       monitor_75 </strong><strong>… </strong><strong>… </strong><strong>– End –  </strong><strong>=========================================================================== </strong> </td>

  </tr>

 </tbody>

</table>




<table width="617">

 <tbody>

  <tr>

   <td width="617"><strong> </strong><strong>*** Room Booking – REJECTED / FCFS *** </strong><strong> </strong><strong>Tenant_A (there are <u>999</u> bookings rejected): </strong><strong> </strong><strong>Date         Start   End     Type          Device </strong><strong>=========================================================================== </strong><strong>2021-05-16   09:00   12:00   Meeting       – </strong><strong>2021-05-17   18:00   21:00   Presentation  projector_4K                                            screen_150 </strong><strong>… </strong><strong>… … … … … … … … … … … … … … … … … … … </strong><strong>… </strong><strong>Tenant_B (there are <u>999</u> bookings rejected): </strong><strong> </strong><strong>Date         Start   End     Type          Device </strong><strong>=========================================================================== </strong><strong>2021-05-13   13:00   15:00   Conference    webcab_UHD                                            monitor_75 </strong><strong>… </strong><strong>… </strong><strong> </strong><strong>– End – </strong><strong> </strong> </td>

  </tr>

 </tbody>

</table>

The “Summary” may have the format as shown below.

<table width="617">

 <tbody>

  <tr>

   <td width="617"> <strong>*** Room Booking Manager – Summary Report *** </strong><strong> </strong><strong>Performance: </strong><strong> </strong><strong>  For FCFS: </strong><strong>          Total Number of Bookings Received: 999 (99.9%) </strong><strong>                Number of Bookings Assigned: 999 (99.9%)                 Number of Bookings Rejected: 999 (99.9%)  </strong><strong>          Utilization of Time Slot:            room_A        – 99.9%            room_B        – 99.9% </strong><strong>… </strong><strong>           webcam_FHD    – 99.9% </strong><strong>… </strong><strong>           projector_4K  – 99.9% </strong><strong>… </strong><strong>… </strong><strong> </strong><strong>          Invalid request(s) made: 999 </strong><strong> </strong><strong>  For PRIO: </strong><strong>          Total Number of Bookings Received: 999 (99.9%) </strong><strong>                Number of Bookings Assigned: 999 (99.9%)                 Number of Bookings Rejected: 999 (99.9%)  </strong><strong>          Utilization of Time Slot:            room_A        – 99.9%            room_B        – 99.9% </strong><strong>… </strong><strong>           webcam_FHD    – 99.9% </strong><strong>… </strong><strong>           projector_4K  – 99.9% </strong><strong>… </strong><strong>… </strong><strong> </strong><strong>          Invalid request(s) made: 999 </strong>  </td>

  </tr>

 </tbody>

</table>




<h2>Error handling</h2>

Although the program does not need to check for the correctness of the format and values that are input by user, some other error handling features are required in the application.  For example, if there are incorrect names of device, RBM should return an error message to indicate that and simply ignore that request.




<h1>Documentation</h1>

Apart from the above program implementation, you are also required to write a project report that consists of following parts:

<ol>

 <li>Introduction (<em>What is the objective of this project?</em>)</li>

 <li>Scope (<em>What operating systems topics have been covered in this project?</em>)</li>

 <li>Concept (<em>What are the algorithms behind?</em>)</li>

 <li>Your own scheduling algorithm (<em>if any</em>)</li>

 <li>Program structure of your application</li>

 <li>Testing cases (<em>In the report, briefly describe what you have done to test the correctness of the program? For the details of the tests, that part should be attached in the section </em></li>

</ol>

<em>“Appendix”.</em>)

<ol start="7">

 <li>Performance analysis (<em>Discuss and analyze the algorithms used in the program, if there are more one algorithm. Why the one you proposed is better than the others?</em>)</li>

 <li>Program set up and execution (<em>How to compile and execute your project? On which Linux server would you like your project to be executed?</em>)</li>

 <li>Appendix – source code; testing data, testing results, and samples of “room booking timetable” &amp; “rejected list” which are generated by your application.</li>

</ol>

<em> </em>

<em>***Noted that you should use a proper report format. </em>

<h1>Demonstration</h1>

The date of demonstration is <em>tentatively</em> scheduled on <strong>April 17 or 18, 2021</strong> (<em>please reserve your time on these days</em>).  There are two parts in the demonstration.  The first part is to make a <strong>video</strong> (<em>in MP4 format</em>) to introduce and demonstrate your application with a dataset which is prepared by your group (<em>length of the demonstration video is about 3 to 5 minutes</em>).  Submit the video together with the <strong>source code</strong> and the <strong>project report</strong> before the due date.




The second part is to have another <strong>video</strong> (<strong>3 to 5 minutes</strong>) to show the execution of your application based on the dataset that provided by us.  A set of <strong>documents of the running results</strong> (<em>which generated by your application</em>) should be submitted to the Blackboard once again (<em>details would be provided later through the Blackboard</em>).  If your application cannot run the provided data normally or successfully, you are allowed to correct/modify your application within a grace period.  The revised/modified source code should be submitted to the Blackboard again.  In addition, you should let us know what error(s) you have encountered and how you fix the problem.




<em>***Note: If the size of the video is too large (cannot upload it to the Blackboard), you may send us a link to download it. </em>







<em>Mark distribution</em>

The mark distribution of this project is as follows:

Implementation:                  60 %

Documentation:                   25 %

Demonstration:     15 % Bonus:   10 %

<strong><em>Bonus</em></strong>

The bonus marks will be awarded for being able to propose and implement your own scheduling algorithm that performs better than AT LEAST ANY ONE of the well-known scheduling algorithms.  In addition, proper use of the two system calls, <strong><sub>pipe()</sub></strong> and <strong><sub>fork()</sub></strong>, may have a certain proportion in the marking.