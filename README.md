# customized-floodlight
Application Aware Data Forwarding in SDN framework



Software-Defined Network is completely new networking paradigm which is grow-
ing rapidly. To have a good understanding of it is must in order to contribute
something from our side. Our aim is to understand the step-by-step execution of
device detection(host and switches), topology figuration, finding the optimal path
by OpenFlow controller(FLoodLight in our case) for packet-in based on shortest
path algorithm(traditional) and so on. Once we are done with it our main fo-
cus is to make module corresponding to process packet and find out type of pay-
load(TCP, UDP, ARP, etc.) coming into it, by statistical estimation we fetch the
bandwidth of links and then divert the packet(let’s say UDP) to path with maxi-
mum bandwidth. We call this widest path. The same concept can be extrapolated
to different cases we come across for optimal packet forwarding.


Objective

The tasks assigned to us were as follows:
• Studying about SDN, Mininet, FloodLight Controller and OpenFlow. Consider
a topology of around 40-50 nodes and 7-8 switches. (for a close to real topology
you can refer to “topology-zoo.”).
• Create a topology with different link properties (i.e., with different bandwidth,
different loss-rate and different latency; you can tweak the parameters using Mininet
Pyhton script.)
• Topology should have multiple paths from source to destination with varied link
characteristics.
• Assume that the end-hosts are running different applications. (Video Streaming,
large file transfers using FTP protocol, and simple HTTP based web access).
• Write a new module in the Floodlight controller, which can first analyse the
type of traffic or application and then create source to destination flow-entries
across switches depending upon the application requirement.(for example: video
streaming needs high bandwidth and low latency path, http based web access can
be made through a low bandwidth path, etc.)
• Verify and show proof that your controller is able to perform application-aware
forwarding.
• Compare the performance of your implementation over the same set of experi-
ments with unmodified controller application.
