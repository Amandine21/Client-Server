# Client-Server
For this project, I created a file transfer which made use of request channels. For this, I made one
function which requested a single point in a csv. Using this, I was able to transfer 1000 points and time
them. With this, it ended up taking quite a long time to process. This would be done by creating a
message asking for the point, sending it over, and receiving the value back. It would then be repeated
until finished.

After processing points, I switched over to transferring files byte by byte. For this, I opened each file
by first requesting the size with a standard request, then changing the standard request to request each
section of the file. Then each section is written to the destination file. From this, we were able to start
modifying the size of each section transferred. This buffer size specifically created one of the possible
bottlenecks in how fast the file transferred. From modifying this, we are able to speed up how fast it
transfers the file. There are many potential bottlenecks outside of this, such as there only being a single
channel to ask for information, the hardware limitations, and more.
