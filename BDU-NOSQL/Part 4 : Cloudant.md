Introducing IBM Cloudant Script
===========================================================

1. List the key benefits of IBM Cloudant, a NoSQL Database-as-a-Service.
2. Describe Cloudant’s architecture.
3. List the features of Cloudant.
4. Explain the problems a Cloudant solution can solve.
5. Describe Cloudant’s deployment options.

----------------------------------------------

This lesson outlines the key benefits of IBM Cloudant, describes its architecture, features, and deployment
options, and explains the types of challenges a Cloudant solution can solve.

Part 1 Benefits
===============

Cloudant aims to be the data layer for all your Web and mobile applications.

* Cloudant is simple to use, but still feature-rich.
* It uses an HTTP API without the need for proprietary drivers and uses a JSON document store, so
development is simplified for modern Web applications by dealing with JSON objects on all layers of the
stack.
* Cloudant uses a flexible schema which means you can iterate on new features for fast and agile
development.
* Cloudant has fully-integrated capabilities for online analytics, full text search, and advanced geospatial
querying along with replication without the need for 3rd-party integrations.
* It’s offered as a fully managed service, or database-as-a-Service, so there are no administrative
headaches.
* Cloudant offers white glove service from big data experts to help you build your applications.
* It includes an easy-to-use dashboard for creating and managing your databases.

#### Cloudant scales…massively.
It scales both in terms of data size and concurrent users.
It’s appropriate for both the startup company who is building an application with 1 GB of data and 10
users to enterprise with petabytes of data/20 million daily active users. Cloudant aligns the cost for both
of these scenarios, and meets performance service level agreements throughout the lifecycle.
Cloudant allows for scaling up/down as.

#### Cloudant is available…always.
* It’s an operational datastore for online applications so building a service that aims to be available
24x7x365 is a must.
* It’s durable – aiming to never lose data by storing multiple copies of all data across separate physical
nodes.
* It’s partition tolerant in order to meet the most stringent high availability disaster recovery requirements,
whether handling node failures in a cluster, or even full data center outages.
* Cloudant is uniquely engineered to patch/upgrade on the fly…no outage necessary! We can upgrade
clusters without taking your database offline.
* It provides offline and online access ideal for when there can be spotty connectivity, for example, in
remote areas and airplanes.

---------------------------------------------------------------------

#### Part 2. Architecture
You have the option to host your data in over 35 data centers. Cloudant is supported on SoftLayer, an IBM
Infrastructure as a Service offering, RackSpace, Azure, or Amazon Web Services, so it’s cloud agnostic.
Cloudant has the most robust and easy-to-use replication protocol; never corrupting the data, thereby
providing the best of any available data layer. 

Cloudant replicates from one data center to another making
the data available throughout the world providing geographic load balancing of the data. If a data center
goes offline, the requests will get routed to another active data center providing high availability and 
disaster recovery as well as optimal performance (users get routed to the data center closest to them – or
more specifically using ping time, users get routed to the data center fastest to them).

For Web and Mobile applications that require offline sync (for example, completing an expense report
offline), Cloudant uses a replication protocol that is compatible with libraries that exist in your browser or
Cloudant provided libraries for building iOS and Android applications for customers to connect to the
internet and replicate data for offline use, update data offline, and then sync when back online.

As an operational data store, Cloudant is a good fit for any web or mobile application. Keep in mind that
Cloudant is not a data warehouse, like Hadoop. Cloudant is a document database type of NoSQL
databases.

Cloudant uses an HTTP API, so it’s a lot like working with a RESTful Web service. It’s meant to fit into a
modern architecture, and fits seamlessly into your service oriented architecture without needing to build
the abstracted layer. The HTTP API lets you interact with the data through a browser or cURL returning in
the JSON format.

Cloudant has fully integrated replication and sync. There are a number of different ways to index and slice
and dice the data. MapReduce is a highly efficient way of crunching data in large data sets, and really
good for doing real-time analytics.

 - ***Search engines*** are very popular with web and mobile application developers. Many applications make
asynchronous calls under the covers for doing full text adhoc search of your data. Other database-as-aservice
offerings require you to integrate with a third-party search engine, such as Elastic Search or
Apache Solar which are both built on Lucene whereas, Cloudant has full text search fully built in to both
the database-as-a-service and local offerings.

- ***GeoSpatial*** is really good for applications involving oil, gas, or transportation, for example, satellites and
transportation vehicles.

Cloudant offers a fully managed service, an on-premise version, or hybrid cloud deployment.
The Cloudant Dashboard provides an easy way to monitor, administer, and develop your databases.
Cloudant Customers lean on Cloudant to solve many data layer challenges.

Cloudant scales easily for an exponentially growing user base when your relational database isn’t scaling
the way you’d like.

Developing and hosting your own databases has proven to be a challenge with limited budgets, time, and
skill set for administration.

Sometimes, you might be building an application from scratch without fully knowing the capacity
requirements. You need a simple and fast way to develop your applications.

With Cloudant, documents are stored in the popular JSON format with a flexible schema. A database is a
logical collection of documents with a single set of access permissions. Documents are organized into
databases for two primary reasons. This first is for security access reasons, as you can apply access roles
(read, write, admin, replicate) at the database level. The second is for querying, as you can’t index or
query within a single API call across databases. Your cluster can hold any number of databases.

When you sign up for a Cloudant account, there are actual physical servers set up that do the work for
you. It runs on a cluster of servers consisting of load balancers and database nodes on the appropriate
hardware.

Cloudant is horizontally scalable meaning you can distribute your database across a cluster. Cloudant
auto-shards data across a cluster meaning that it auto-partitions the data evenly across clusters. So, you
don’t need to manually distribute the data as you would with a relational data store.

You can start with a small number of nodes, and let Cloudant run scripts to manage your data as it grows
to keep your data available. This means you don’t have to do much capacity planning up front because

Cloudant can easily adapt as your data needs increase and maintain performance.
The data is replicated within the cluster to keep them synchronized without any administrative
intervention. If a node fails and is then brought back online, it will automatically be brought up-to-date
using replication to sync the data.

To replicate across geos or clusters, you can configure when and how that replication will happen.
If you’re storing data across a cluster, it doesn’t really do you any good to store one copy on one node
because if the node fails, then you’ll lose the data and it will become unavailable to your applications.

Cloudant employs a quorum-style clustering which stores every JSON document in triplicate across three
separate physical nodes. When your application reads and writes data, Cloudant uses a load balancer that
distributes the reads and writes evenly across the cluster so the workload is distributed. So if one node
fails, the data is still available on another node.

#### Deployment
For deployment options, Cloudant offers both managed and local product offerings. The fully managed
service eliminates your having to set up and manage the infrastructure. Cloudant local is available for
those customers who have a strict proprietary policy for keeping data local in a private data center.

Unless you have your own data centers or have strong data privacy concerns, you’ll probably want to use
the Cloudant database-as-a-service. You can sign up for a Cloudant Multi-tenant account at Cloudant.com
and use it for development or prototyping. 

And for Managed database-as-a-service production deployment, we recommend Cloudant Dedicated, where we set up your Cloudant account on dedicated, single-tenant clusters in the SoftLayer, Rackspace, Amazon, Azure data center(s) of your choice. Cloudant
Dedicated costs a recurring monthly fee based on how many servers are in your cluster.

Alternatively, you can run Cloudant Local…
it’s virtually the same system as Cloudant database-as-aservice,
but deployed to the private cloud infrastructure of your choice and managed by you. Cloudant
Local can be licensed on a perpetual or month-to-month basis, and it includes all the DevOps tooling

Cloudant uses to run its public cloud database-as-a-service offering for easier, safer deployment
