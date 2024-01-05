# Dotnet-WebAPI-Caching

## What is cache?
<b>Caching is storing data in a special place for faster access to it in the future.</b>


### Types of caching in .NET Core
#### In-Memory Cache —
 caching stores and receives the results of cached data from the server on which the application is running.

This type of caching is suitable for small or medium applications, which consist of only one server.

In-Memory Cache has drawbacks, what happens with the data if this server restarts or crashes? Obviously they will disappear :) Of course, this can be useful at the development stage, but in production this behavior is unacceptable.

Also with this type of cache, another problem arises, how to access data from another server? Because an application can have multiple servers or can be part of web-farm.

There is one technique for In-Memory Cache — <b>sticky sessions</b>. Sticky sessions means one session always goes to one specific server behind the load balancer.



#### Distributed Cache — 
the cache is not contained in the memory of a specific server, instead some other nodes can be used for storing cached data. Thus every server will have access to the cache and even if the server restarts or crashes, the cached data will not be lost.

for more details visit the following link. 
<herf>
https://blog.devgenius.io/in-memory-and-distributed-cache-net-core-9be16bec34d7</herf>
