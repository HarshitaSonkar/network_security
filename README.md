# network_security

Consider the following simple and small cloud computation scenario:-
Suppose there are four computers, viz., M1– M4. M1 acts as an End-Client which 
can send service requests to M2 which acts as the Service Coordination Server (SCS). The service request 
sent by the client is actually a computation service request where some mathematical computation is 
requested on some data. However, the input data is not sent by the client machine rather; it’s service request 
includes some data-ID which uniquely identifies some data. The SCS has access to M3 acting as a Compute 
Server and M4 acting as a Data Server. All data are kept at the data server, each individual data uniquely 
identified by it’s data-ID (for example data kept in a file in tabular format where each row of the table is an 
individual data identified by the unique row-id). The compute server can perform a limited set of 
mathematical computations. Each of these computations take data as input which should be in the same 
format as that of the individual data kept in the data server. The SCS, after receiving the service request 
from the client, first retrieves the required data from the data server and then sends the appropriate 
computation request along with the input data to the compute server. When compute server returns back 
the result, the SCS forwards it to the client back.

Implement the above described scenario on four inter-connected machines in your lab (Desktop / 
Laptop). Each ‘Role’ (End-Client, SCS etc.) should be implemented as a separate C/C++ Program running 
in one of the four machines. All of the four programs are written as application programs which take the 
services of the transport layer of the UNIX networking stack to implement inter-program communications. 
There are three different inter-program (and inter-computer also) communications, viz., i) between Client 
Program and SCS Program ii) between SCS Program and Data Server Program and iii) between SCS
Program and Compute Server Program. Your codes should also be capable of handling possible error
situations – e.g., ‘data-ID not found error’, ‘invalid service request error’ and ‘communication failure error’ 
etc.
