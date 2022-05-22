---
title: Hadoop - 1. Introduction
date: 2022-03-21 17:15:00
categories:
- [Java, Big Data, Hadoop]
tags: 
- [Java, Hadoop, BigData]
---

# Hadoop - 1. Introduction

### What's Hadoop?

1. Hadoop is a distributed system infrastructure developed by the Apache Foundation
2. Mainly solve, the storage of massive data and the analysis and calculation of massive data
3. Broadly speaking, Hadoop usually refers to a broader concept - the Hadoop ecosystem, including HBASE, HIVE, etc

![image-20220321161607259](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321161607259.png)

<!--more-->

### What are the advantages of Hadoop?

1. High reliability: The bottom layer of Hadoop maintains multiple copies of data, so even if a computing element or storage of Hadoop fails, it will not cause data loss
2. High scalability: Distribute task data among clusters, which can easily scale to thousands of nodes
3. Efficiency: Under the idea of MapReduce, Hadoop works in parallel to speed up task processing
4. High fault tolerance: the ability to automatically reassign failed tasks

### Components of Hadoop

![image-20220321162446307](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321162446307.png)

Hadoop3.x has no change in composition compared to Hadoop2.x

### Overview of Hadoop Distributed File System (HDFS)

1. NameNode (nn): Stores file **metadata**, such as **file name, file directory structure, file attributes (generation time, number of replicas, file permissions)**, and the list of **blocks for each file** and **the DataNode where the block resides**, etc.
2. DataNode (dn): Store **file block data** in the local file system, as well as **checksums of the block data**.
3. Secondary NameNode (2nn): Backup NameNode metadata at regular intervals

### Overview of Yet Another Resource Negotiator (YARN)

- Resource Manager (RM): Manage the entire cluster resources (memory, cpu, etc.)
- Node Manager (NM): Manage single node server resources
- Application Master (AM): Manage individual task
- Container: It is equivalent to an independent server, which encapsulates the resources needed to run tasks, such as **memory, cpu, disk, network, etc**.

![image-20220321163802165](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321163802165.png)

Reminder:

1. Clients can be multiple
2. Multiple Application Masters can run on the cluster
3. There can be multiple Containers on each Node Manager

### Overview of MapReduce

MapReduce divides the computing process into two stages: Map and Reduce

1. Map processes the input data in parallel
2. Reduce summarizes the results of Map

![image-20220321165315360](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321165315360.png)

### Relationship Between HDFS, YARN and MapReduce

![image-20220321165928634](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321165928634.png)

### Technology Ecosystem

![image-20220321170920278](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321170920278.png)

![image-20220321171129463](https://raw.githubusercontent.com/2855239858/myBlog/8b593413bf68f64198bc4db50da340a78c6f4813/source/_posts/Hadoop%20-%201.%20Introduction.assets/image-20220321171129463.png)