# comp3500--introduction-to-operating-systems-project-3---synchronization-mechanisms-short-version-1
**TO GET THIS SOLUTION VISIT:** [COMP3500-  Introduction to Operating Systems Project 3 – Synchronization Mechanisms Short Version: 1](https://mantutor.com/product/comp3500-introduction-to-operating-systems-project-3-synchronization-mechanisms-short-version-1-0-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top kksr-disabled" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;80498&quot;,&quot;readonly&quot;:&quot;1&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP3500-  &nbsp;Introduction to Operating Systems  Project 3 – Synchronization Mechanisms  Short Version: 1.0 - Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<strong>Objectives:&nbsp; </strong>

<ul>
<li>To implement the lock mechanism</li>
<li>To implement condition variables</li>
<li>To improve your source code reading skills</li>
<li>To strengthen your debugging skill</li>
</ul>
<strong>&nbsp;</strong>

<h1>1. Project Goals</h1>
This project assignment provides you with the opportunity to learn how to implement basic synchronization mechanisms covered in our lectures. You have to be familiar with the OS/161 thread code in order to accomplish this project. Note that the thread system is comprised of interrupts, control functions, and semaphores. Please keep in mind that the goal of this project is to implement locks and condition variables.

&nbsp;

<h1>2. Getting Started</h1>
<strong>2.1 Setup </strong><strong>$PATH </strong>

export PATH=~/cs161/bin:$PATH

&nbsp;

<h2>2.2 Create a New Git Repository</h2>
This project does not rely on Project 2 and; therefore, you will start with a new Git repository. You should be able to keep the root directory, as the necessary files are automatically overwritten.

<strong>&nbsp;Important! </strong>&nbsp;This step is very important; please follow the instructions carefully.

%cd ~/cs161

%mkdir archive

%mv src archive/src-project2

%tar vfzx os161-1.10.gz

%mv os161-1.10 src

%cd src

%git init&nbsp;&nbsp; %git add .

%git commit -m “ASST1a initial commit”

&nbsp;

Prior to working on this project, please tag your Git repository (See the following command below). The purpose of tagging your repository is to ensure that you have something against which to compare your final tree.

%git tag asst1a-start

<strong>&nbsp;</strong>

<h2>2.3 Project Configuration</h2>
You are provided with a framework to run your solutions for this project. This framework consists of driver code (found in kern/asst1) and menu items you can use to execute your solutions from the OS/161 kernel boot menu.

&nbsp;

You must reconfigure your kernel before you can use this framework. The procedure for configuring a kernel is the same as in ASST0, except you will use the ASST1 configuration file.

%cd ~/cs161/src

%./configure

%cd kern/conf

%./config ASST1

&nbsp;

<h2>2.4 Building for ASST1</h2>
You can follow the three commands to build OS/161 for this project.

%cd ~/cs161/src/kern/compile/ASST1

%make depend

%make

%make install

Please place sys161.conf in your OS/161 root directory (~/cs161/root).

<strong>&nbsp;</strong>

<h2>2.5 Command Line Arguments to OS/161</h2>
Your solutions to this project (a.k.a., ASST1) will be tested by running OS/161 with command line arguments that correspond to the menu options in the OS/161 boot menu.

<strong>&nbsp;</strong>

<h2>2.6 Physical Memory</h2>
You are advised to allocate at least 2MB of RAM to System/161. This configuration option is passed to the busctl device with the ramsize parameter in your sys161.conf file. The busctl device line looks like the following line, where 2097152 bytes is 2MB.

31 busctl ramsize=2097152

&nbsp;

<h1>3. Concurrent Programming with OS/161</h1>
If your code is properly synchronized, it is guaranteed that the timing of context switches and the order in which threads run will not change the behavior of your solutions.

<h2>3.1 Built-in Thread Tests</h2>
<strong>&nbsp;Important! </strong>&nbsp;&nbsp;When you booted OS/161 in project 2 (a.k.a., ASST0), you may have seen the options to run the thread tests. The thread test code makes use of the semaphore synchronization primitive. You should be able to trace the execution of one of these thread tests in cs161-gdb to see how the scheduler acts, how threads are created, and what exactly happens in a context switch.

&nbsp;

Thread test 1 ( ” tt1 ” at the prompt or tt1 on the kernel command line) prints the numbers 0 through 7 each time each thread loops. Thread test 2 (” tt2 “) prints only when each thread starts and exits. The latter is intended to show that the scheduler doesn’t cause any starvation (e.g., the threads should all start together, run for a while, and then end together).

<strong>&nbsp;</strong>

<strong>3.2 Debugging Concurrent Programs </strong>thread_yield() is automatically called for you at intervals that vary randomly. This randomness is fairly close to reality, but it complicates the process of debugging your concurrent programs. You can pass an explicit seed into random device by editing the “random” line in your sys161.conf file. For example, to set the seed to 1, you would edit the line to look like:

28 random seed=1

&nbsp;

<strong>&nbsp;Important! </strong>&nbsp;&nbsp;It is strongly recommended that while you are writing and debugging your solutions you pick a seed and use it consistently. Once you are confident that your threads do what they are supposed to do, set the random device to autoseed. This allows you to test your solutions under varying conditions and may expose scenarios that you had not anticipated.

&nbsp;

<h1>4. Code-Reading Exercises</h1>
Please answer the following questions related to OS/161 threads. Please place answers to the following questions in a file called codereading.txt. You should store

codereading.txt in directory “~/cs161/project3”. If you haven’t yet created this directory, please run the following three commands. The touch command creates an empty text file named codereading.txt. You may use any text editor (e.g., vi) to modify this file.

%cd ~/cs161

%mkdir project3

$touch codereading.txt

<strong>&nbsp;</strong>

<h2>4.1 Thread Questions</h2>
<ul>
<li>What happens to a thread when it exits (i.e., calls thread_exit() )? What about when it sleeps?</li>
<li>What function(s) handle(s) a context switch?</li>
<li>How many thread states are there? What are they?</li>
<li>What does it mean to turn interrupts off? How is this accomplished? Why is it important to turn off interrupts in the thread subsystem code?</li>
<li>What happens when a thread wakes up another thread? How does a sleeping thread get to run again?</li>
</ul>
<strong>&nbsp;</strong>

<h2>4.2 Scheduler Questions</h2>
<ul>
<li>What function is responsible for choosing the next thread to run?</li>
<li>How does that function pick the next thread?</li>
<li>What role does the hardware timer play in scheduling? What hardware independent function is called on a timer interrupt?</li>
</ul>
<strong>&nbsp;</strong>

<h2>4.3 Synchronization Questions</h2>
<ul>
<li>Describe how thread_sleep() and thread_wakeup() are used to implement semaphores. What is the purpose of the argument passed to thread_sleep()?</li>
<li>Why does the lock API in OS/161 provide lock_do_i_hold(), but not lock_get_holder()?</li>
</ul>
<strong>&nbsp;</strong>

<h1>5. Programming Exercises</h1>
<h2>5.1 Synchronization Primitives: Implementing Locks</h2>
In the first programming exercise of project 3, you will implement locks for OS/161. The interface for the lock structure is defined in kern/include/synch.h. Stub code is provided in kern/thread/synch.c.

&nbsp;

<h2>5.2 Synchronization Primitives: Implementing Condition Variables (<em>CV</em>)</h2>
Implement condition variables for OS/161. The interface for the cv structure is also defined in synch.h and stub code is provided in synch.c.
