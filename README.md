# A-personal-recommender-system-based-on-an-unweighted-graph
topic: Big Data; MapReduce; Hadoop; Breadth-first search

# ABSTRACT

Nowadays, many organizations, companies and researchers need
to deal with big datasets in the order of terabytes or even
petabytes. A popular data processing engine for handling such big
datasets in an efficient way is Hadoop MapReduce. These big
datasets are often represented as graphs by many systems of
current interest (i.e. Internet, social network). A key feature of
these systems is provided by personalized recommender systems
for information retrieval and content discovery in today’s
informationrich environment. Usually modern recommendation
systems use complex technique to provide advices to each user. In
this paper we explain our implementation of different way to
provide recommendations to users of a network based on an
unweighted graph. Using an Hadoop iterative MapReduce
approach for the implementation.

# INTRODUCTION

MapReduce is a programming model and an associated
implementation for processing and generating very large data sets
with parallel and distributed algorithm on a cluster. MapReduce
has been ideated by Google's researcher Jeffrey Dean and Sanjay
Ghemawat in 2004 for handling large data sets which are usually
computed by hundreds or thousands machines to finish in the
shortest possible period [1].
MapReduce works through two functions called Map() and
Reduce(). The Map() function takes an input element and
generated a set of intermediate key-value pairs and passes it to the
Reduce() function. The Reduce() function takes the set of the
intermediate key-value pairs, merges all the intermediate values
for a particular key and produces a smaller set of merged output
values.
The power of MapReduce is that it allows programmers without a
deep experience in parallel and distributed systems to easily
utilize the resource of a large distributed system, breaking a
computation into small tasks that run in parallel on multiple
machines, and scales easily to very large clusters of inexpensive
commodity computers. Moreover, another key benefit of
MapReduce is that it automatically handles failures, hiding the
complexity of fault-tolerance from the programmer. In fact if a
node crashes, MapReduce runs the task on a different machine
[2].
A popular implementation of MapReduce is the open-source
framework Apache Hadoop [3]. It was developed mainly by
Yahoo! though is also used by other companies, such as
Facebook, Amazon and Last.fm [4]. One of the characteristic of
Hadoop is the use of HDFS (Hadoop distributed file system)
which was designed to store a massive amount of data, in order to
optimize storage and access operations to a small number of large
file, rather than a lot of small file [5].
Nowadays, many systems of current interest to the scientific
community can usefully be represented as graphs [6]. Some
examples include the world-wide web, the Internet, social
networks, citations of papers, food webs, biochemical networks
and many more. Each of these networks consists of a set of nodes
representing, for instance, computers or routers on the Internet or
people in a social network, connected each other by edges,
representing data connections between computers, friendships
between people, and so forth. Often these graphs are made up of a
huge amount of nodes and edges.
In the following sections is described our idea and the
implementations of work that was done. We thought about a
different way to provide recommendations to users of a networks.
Our program aims to visit a unweighted graph starting from a set
of nodes (also called keynodes) to find out which nodes can be
reached by the keynodes within a adjustable maximum distance. It
has been implemented using MapReduce in order to handle big
datasets.
This paper is organized as follows. Section 2 describes related
works which has been used as starting point for our
implementation of the project. Section 3 presents the problem we
are trying to solve whereas section 4 provides our solution and
implementation. Section 5 describes all the experiments we
performed using different sets of data. Finally, we conclude in
section 6.

For the whole report open the file report.pdf
