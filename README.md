# distributed-systems-lab-4-solved
**TO GET THIS SOLUTION VISIT:** [Distributed Systems Lab 4 Solved](https://www.ankitcodinghub.com/product/distributed-systems-lab-4-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100299&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Distributed Systems Lab 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Laboratory 4

In this laboratory activity, you are invited to practice with the TCP/IP socket API, the de- facto standard API for accessing network services from layers 4-3-2 in the Internet.

The activity is comprehensive of the following tasks:

<ul>
<li>implementation of a TCP/IP socket server application (in Java);</li>
<li>implementation of a TCP/IP socket client application (in Java).
The tool that is recommended for the development of the solution is:

▪ Eclipse IDE for Enterprise Java Developers for the development of the TCP/IP socket

server and client.

Context of the activity

The Converter service is a concurrent TCP server, listening to the TCP port number 2001, which can perform the media type conversion of image files. The media types supported by this service are three: PNG, JPEG, and GIF. The server is able to establish TCP connec- tions with multiple clients; each request is managed by a different thread.

The ConversionRequest client is an application that must interact with the Converter ser- vice to perform the conversion of an image file. This applications receives three parame- ters from the command line:
</li>
</ul>
<ol>
<li>the original media type of the image file;</li>
<li>the target media type to which the image file must be converted;</li>
<li>the path of the image file in the local file system of the ConversionRequest client.</li>
</ol>
After checking that the file exists, the client establishes a TCP connection with the Con- verter service. On this connection, the following protocol is followed. When the TCP con- nection is successfully established, the client sends to the server:

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
<ul>
<li>three ASCII characters (1 byte for each character), representing the original media type of the image file that must be converted. The allowed sequences of ASCII characters are PNG, JPG and GIF;</li>
<li>three ASCII characters (1 byte for each character), representing the media type to which the image file must be converted. The allowed sequences of ASCII characters are PNG, JPG and GIF;</li>
<li>a 4-byte 2’s complement integer number in network byte order, representing the length in bytes of the image file that must be converted;</li>
<li>the bytes of the image file that must be converted.
The following picture illustrates an example of a client request to convert a file image from PNG to JPEG media type. The bytes L1, L2, L3, L4 represent the file length; the bytes F1, F2, …, FL represent the content of the file to be converted.

After the server has successfully received all these pieces of information from the client, it converts the file to the requested media type. Then, it sends to the client:
</li>
</ul>
<ul>
<li>the ASCII character ‘0’ (1 byte) representing the successful outcome of the receiv- ing and conversion operations;</li>
<li>a 4-byte 2’s complement integer number in network byte order, representing the length in bytes of the converted image file;</li>
<li>the bytes of the converted image file.

Finally, the server starts the procedure for gracefully closing the connection.

After having received the file and having saved it locally, the client completes the closing of the TCP connection.

The following picture illustrates an example of a server response in the case that all the operations are successful. The bytes L1, L2, L3, L4 represent the length of the converted file; the bytes F1, F2, …, FL represent the contents of the converted image file.
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
Instead, in case there are issues in receiving the message sent by the client or in convert- ing the image file, the server sends to the client:

<ul>
<li>an ASCII character (1 byte) representing a number greater than 0 in case of unsuc- cessful outcome for the receiving or conversion operation (more specifically, the ASCII character is ‘1’ for a wrong request, ‘2’ for internal error of the server);</li>
<li>a 4-byte integer number in network byte order, representing the length in bytes of a string describing the error that occurred;</li>
<li>the bytes of an ASCII string describing the error that occurred.
The following picture illustrates an example of a server response in the case that the re- ceiving or conversion operation has failed because of an internal error of the server. The bytes L1, L2, L3, L4 represent the length of the error message; the bytes E1, E2, …, EL repre- sent the content of the error message.

How to test your client and server

Try the conversion of files of different types and check that the received converted file is correct (i.e., it can be opened by a viewer without errors). Try a conversion with a file of large size (e.g. 10MB) and check that your protocol implementation is still correct, and efficient in transferring the files in terms of transfer time. Run more clients concurrently and check how execution time varies.

Test interoperability by testing your client and server against the reference client and server provided with the lab material. In order to execute the reference client and server, you must use the following commands in their local directories:
</li>
</ul>
<ul>
<li>java -jar client.jar &lt;original_type&gt; &lt;target_type&gt; &lt;image_path&gt;</li>
<li>java -jar server.jar
The images to be converted must be put in the “image” folder of the directory where the client.jar is executed.
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Test and improve the robustness of your client and server

Both the client and the server should use timeouts when waiting for input from the peer, in order to avoid deadlocks.

Try your client and server under erroneous conditions and fix any robustness problems:

<ul>
<li>Try to connect the client to a non-reachable address.</li>
<li>Try to stop a client before it has completed its operation (by pressing ^C in its
window) and check that the server recovers correctly from this error.
</li>
<li>Try to stop the server (by pressing ^C in its window) while a client is connected
and check that the client manages the error.

How to experience this laboratory activity

You are invited to complete both the tasks required to fully carry out this laboratory ac- tivity (i.e., development of the TCP server and client). However, you can reuse the Java code that performs the image conversion from the Java Converter service, published as solution for the second Laboratory activity.

For the implementation of concurrency in the server-side, you can use the ExecutorServ- ice framework provided by the JDK, since it simplifies the execution of tasks in asynchro- nous mode (https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/Execu- torService.html ).

In order to avoid synchronization problems (e.g. race conditions) between different threads in the server, it is suggested to avoid write operations on shared variables.
</li>
</ul>
</div>
</div>
</div>
