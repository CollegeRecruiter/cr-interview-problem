# College Recruiter Interview


You will find in a link; a google drive file with temperatures listed as `temps.txt`. These are temperatures listed in celsius. 

Your mission is to create a simple REST API written in Node.js to convert these temperatures to fahrenheit and should include instructions on how to start the program and some core design decisions you made in a brief summary. We don't want this last more than an hour for you at most.

You will notice this is a large file. The requirements for this API are simple but first some important things are that ok to do.

1. The file is located on the same server as the Node.js program/server. Thus you have direct access and don't need to provide some sort of upload functionality.

2. Improvements to the process are welcome IE: hosted servers etc, custom libraries etc. Show us what you got!


The requirements for the API are as follows:

1. The API should contain a `/start` endpoint to begin the conversion.
2. The API should contain a `/end` to end the conversion.
3. The API should provide a `/status` endpoint to provide the progress of the the conversion .
4. The API should contain a `/result` to download the converted file at any time in the process.
4a. The result should return the file at any stage of the conversion process.

5. The API does not need to be stable across multiple calls of `/start`. 
6. The API must be stable to get a `/result` when calling `/end` and provide partial conversion of the `temps`. IE: Run the `/start` for 10 seconds, call `/end` to stop the conversion and call `/result` to get what has processed so far.
7. The api can be started again by calling `/start` and the file continues where it left off on the conversion so work is not repeated.