# PageRank-Hadoop
To Run the project  Start a newProject in Eclipse and all the <code>.java files</code>

After That import the external JARs
  1. hadoop-core-2.X  
  2. hadoop-common-2.X
Make sure the version are > 2.0  Otherwise it give an compliation error (Class is found instead of Interfrace)

Export the Project as a JAR 

After that follow these steps.<br>
<b>NOTE: Make sure that your hadoop is up and running.</b>
<code>
1. <code>hdfs dfs -mkdir "Input Directory"</code>
2. <code>hdfs dfs -put "Input file name"  "Input Directory" .</code>  (any file from web-graph tab from <a href="https://snap.stanford.edu/data/">here</a>)
3. <code>hdfs dfs jar JAR_Filename.PageRank --input "Full path to input Direcotory in HDFS" --output "Full path for output path in HDFS".</code>

NOTE: Output directory need not to be already existing.

After completion of process you can find 4 different folders in the output directory 
  iter00,iter01,iter02,result
  
 These contains result after different iteration and the last one contains the result in sorted order.

<b>NOTE: You can change the dmping factor and no of iterations in PageRank.java file</b>
