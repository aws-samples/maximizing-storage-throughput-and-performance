# **Maximizing Storage Throughput and Performance**

© 2019 Amazon Web Services, Inc. and its affiliates. All rights reserved.
This sample code is made available under the MIT-0 license. See the LICENSE file.

Errors or corrections? Contact [mburbey@amazon.com](mailto:mburbey@amazon.com).
---
## Workshop Summary

In this workshop you learn how to obtain higher levels of performance with EBS, S3 and EFS.

#### 1. Deploy AWS resources using CloudFormation

1. Click one of the launch links in the table below to deploy the resources using CloudFormation.  To avoid errors during deployment, select a region in which you have previously created AWS resources.

  | **Region Code** | **Region Name** | **Launch** |
  | --- | --- | --- |
  | us-west-1 | US West (N. California) | [Launch in us-west-1](https://console.aws.amazon.com/cloudformation/home?region=us-west-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | us-west-2 | US West (Oregon) | [Launch in us-west-2](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | us-east-1 | US East (N. Virginia) | [Launch in us-east-1](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | us-east-2 | US East (Ohio) | [Launch in us-east-2](https://console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ca-central-1 | Canada (Central) | [Launch in ca-central-1](https://console.aws.amazon.com/cloudformation/home?region=ca-central-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | eu-central-1 | EU (Frankfurt) | [Launch in eu-central-1](https://console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | eu-west-1 | EU (Ireland) | [Launch in eu-west-1](https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | eu-west-2 | EU (London) | [Launch in eu-west-2](https://console.aws.amazon.com/cloudformation/home?region=eu-west-2#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | eu-west-3 | EU (Paris) | [Launch in eu-west-3](https://console.aws.amazon.com/cloudformation/home?region=eu-west-3#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | eu-north-1 | EU (Stockholm) | [Launch in eu-north-1](https://console.aws.amazon.com/cloudformation/home?region=eu-north-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-east-1 | Asia Pacific (Hong Kong) | [Launch in ap-east-1](https://console.aws.amazon.com/cloudformation/home?region=ap-east-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-northeast-1 | Asia Pacific (Tokyo) | [Launch in ap-northeast-1](https://console.aws.amazon.com/cloudformation/home?region=ap-northeast-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-northeast-2 | Asia Pacific (Seoul) | [Launch in ap-northeast-2](https://console.aws.amazon.com/cloudformation/home?region=ap-northeast-2#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-northeast-3 | Asia Pacific (Osaka-Local) | [Launch in ap-northeast-3](https://console.aws.amazon.com/cloudformation/home?region=ap-northeast-3#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-southeast-1 | Asia Pacific (Singapore) | [Launch in ap-southeast-1](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-southeast-2 | Asia Pacific (Sydney) | [Launch in ap-southeast-2](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-2#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | ap-south-1 | Asia Pacific (Mumbai) | [Launch in ap-south-1](https://console.aws.amazon.com/cloudformation/home?region=ap-south-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | me-south-1 | Middle East (Bahrain) | [Launch in me-south-1](https://console.aws.amazon.com/cloudformation/home?region=me-south-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |
  | sa-east-1 | South America (São Paulo) | [Launch in sa-east-1](https://console.aws.amazon.com/cloudformation/home?region=sa-east-1#/stacks/new?stackName=StoragePerformanceWorkshop&amp;templateURL=https://storage-specialists-cf-templates.s3-us-west-2.amazonaws.com/2019/storage_performance.json) |

2. Click  **Next**  on the Create Stack page.
3. Click  **Next**.
4. Click  **Next**  Again. (skipping the Options and Advanced options sections)
5. On the Review page, scroll to the bottom and check the boxes to acknowledge that CloudFormation will create IAM resources, then click  **Create stack**.  

  ![](/images/mod1cf1.png)
6. Click **Events**. Events will not auto refresh.  You will need to manually refresh the page using the refresh button on the right side of the page.  
7. Watch for **StoragePerformanceWorkshop** and a status of **CREATE_COMPLETE**  

  ![](/images/cf_complete.png)  

**Note:** Instances that are launched as part of this CloudFormation template may be in the initializing state for few minutes.  

#### 2. Connect to the EC2 Instance using EC2 Instance Connect

1. From the AWS console, click  **Services**  and select  **EC2.**  
2. Select  **Instances**  from the menu on the left.  
3. Wait until the state of the S3_Workshop_Instance01 instance  shows as _running_ and all Status Checks have completed (i.e. **not** in _Initializing_ state).  
4. Right-click on the **S3_Workshop_Instance01** instance and select  **Connect** from the menu.  
5. From the dialog box, select the EC2 Instance Connect option, as shown below:

  ![](/images/mod1ssh1.png)

6. For the **User name** field, enter "ec2-user", then click **Connect**. A new dialog box or tab on your browser should appear, providing you with a command line interface (CLI).  Keep this open - you will use the command line on the instance throughout this workshop.  
7. Verify your login prompt contains storage-workshop.  If it does not the initialization task for the workshop have not yet completed.  Close the SSH window and repeat the EC2 Instance Connect steps in a couple minutes.  

  ![](/images/cli_1.png)  

Note: The SSH session will disconnect after a period of inactivity. If your session becomes unresponsive, close the window and repeat the steps above to reconnect.  

## EBS Performance Part 1

FIO was automatically launched by the CloudFormation template.  We will use FIO to exhaust the burst credits on the 1 GB GP2 volume.

1. Run the following command to ensure FIO is running on the instance.  Output should be similar to below.
  $ ps -ef | grep fio

  ![](/images/ebs_part1_1.png)
2. From the AWS console, click  **Services**  and select  **EC2.**  
3. Select  **Instances**  from the menu on the left.  
4. Select the instance named **Storage_Performance_Workshop**.  

  ![](/images/ebs_part1_2.png)
5. Click on **/dev/sdb** in the lower pane by Block devices.

  ![](/images/ebs_part1_3.png)
6. In the pop up window, click the **EBS ID**.

  ![](/images/ebs_part1_4.png)  
7. Click on the **Monitoring** tab.  
8. There are two graphs of interest: Read Throughput and Burst Balance.  
   1. Read Throughput should be at 3000 OPS until the Burst Balance is not exhausted.  
   2. Burst Balance will start out at 100% and will decrease steadily over the next 30 minutes.   
9. We will come back to EBS performance later, giving the Burst Balance a chance to be exhausted.  

## S3 Performance- Optimize Throughput of Large Files

In the section we will demonstrate parallelization of a large object by breaking it into smaller chunks and increasing the number of threads used to transfer the object.

1. In the CLI for the instance, run the following commands to setup the AWS CLI

  $ aws configure

  Leave Access Key and Secret Key blank, set the region to the region you deployed your CloudFormation template in , output format leave default.

  ![](/images/aws_configure.png)

2. Configure AWS CLI S3 settings, by running the following commands.

  $ aws configure set default.s3.max_concurrent_requests 1  
  $ aws configure set default.s3.multipart_threshold 64MB  
  $ aws configure set default.s3.multipart_chunksize 16MB  

**Note**  
Commands starting with aws s3 will use the settings above. Any commands starting with aws s3api will not.  aws s3 utilizes Transfer Manager which can optimize transfers.  aws s3api simply makes the specific api call you specified.

3. Verify settings match screenshot below.

  $ cat ~/.aws/config

  ![](/images/s3_perf_1.png)  
4. Run the following command to create a 5 GB file.
  $ dd if=/dev/urandom of=5GB.file bs=1 count=0 seek=5G  

5. Upload a 5 GB file to the S3 bucket using 1 thread.  Record time to complete.  
  $ time aws s3 cp 5GB.file s3://${bucket}/upload1.test   

6. Upload a 5 GB file to the S3 bucket using 2 threads. Record time to complete.  
  $ aws configure set default.s3.max_concurrent_requests 2  
  $ time aws s3 cp 5GB.file s3://${bucket}/upload2.test  

7. Upload a 5 GB file to the S3 bucket using 10 threads. Record time to complete.  
  $ aws configure set default.s3.max_concurrent_requests 10  
  $ time aws s3 cp 5GB.file s3://${bucket}/upload3.test  

8. Upload a 5 GB file to the S3 bucket using 20 threads. Record time to complete.  
  $ aws configure set default.s3.max_concurrent_requests 20   
  $ time aws s3 cp 5GB.file s3://${bucket}/upload4.test  

  At some point the AWS CLI will limit the performance that can be achieved.  This is likely the case if you didn't see any performance increase between 10 and 20 threads.  

9. Run the following command to create a 1 GB file.  
  $ dd if=/dev/urandom of=1GB.file bs=1 count=0 seek=1G  

10. Upload 5 GB of data to S3 by uploading five 1 GB files in parallel. Record time to complete.    
  $ time seq 1 5 | parallel --will-cite -j 5 aws s3 cp 1GB.file s3://${bucket}/parallel/object{}.test

**Note**  

1. These exercises showed that workloads can parallelized by breaking up a large object into chunks or by having smaller files.  
2. One trade off to keep in mind is each PUT is billed at $0.05 per 1,000 requests.  When you break up a 5GB file into 16MB chunks, that results in 313 PUTs instead of  1 PUT.  Essentially you can view it as paying a toll to go faster.  

## S3 Performance- Optimize the Sync command

This exercise will use the aws s3 sync command to move 2,000 files totally 2 GB of data.    

1. In the CLI for the instance, perform the sync using 1 thread.  Record time to complete.  
  $ aws configure set default.s3.max_concurrent_requests 1  
  $ time aws s3 sync /ebs/tutorial/data-1m/ s3://${bucket}/sync1/  

2. Perform the sync using 10 threads.  Record time to complete.  
  $ aws configure set default.s3.max_concurrent_requests 10  
  $ time aws s3 sync /ebs/tutorial/data-1m/ s3://${bucket}/sync2/  

## S3 Performance- Optimize Small File Operations

This exercise will demonstrate how to increase the transactions per second(TPS) while moving small objects.  

1. In the CLI for the instance, create a text file that represents a list of object ids.  
  $ seq 1 500 > object_ids  
  $ cat object_ids  

2. Create a 1 KB file.   
  $ dd if=/dev/urandom of=1KB.file bs=1 count=0 seek=1K  

3. Upload 500 1KB files to S3 using 1 thread.  Record time to complete.  
  $ time parallel --will-cite -a object_ids -j 1 aws s3 cp 1KB.file s3://${bucket}/run1/{}

4. Upload 500 1KB files to S3 using 10 threads. Record time to complete.  
  $ time parallel --will-cite -a object_ids -j 10 aws s3 cp 1KB.file s3://${bucket}/run2/{}   

5. Upload 500 1KB files to S3 using 50 threads. Record time to complete.  
  $ time parallel --will-cite -a object_ids -j 50 aws s3 cp 1KB.file s3://${bucket}/run3/{}  

6. Upload 500 1KB files to S3 using 100 threads. Record time to complete.  
  $ time parallel --will-cite -a object_ids -j 100 aws s3 cp 1KB.file s3://${bucket}/run4/{}  

**Note**  
Going from 50 to 100 threads likely didn't result in higher performance.  For ease of demonstration we are using multiple instances of the AWS CLI to show a concept.  In the real world developers would create thread pools that are much more efficient than our demonstration method.  It is reasonable to assume that added threads should continue to add performance until another bottleneck like running out of CPU occurs.  

## S3 Performance- Optimize Copying Objects to Different Locations

In this exercise we will demonstrate how to copy files from one location in S3 to another more efficiently.  

1. In the CLI for the instance, run this command to download a 5 GB file from the S3 bucket that was uploaded in an earlier test and the upload to a different prefix.  Record time to complete.  
  $ time (aws s3 cp s3://$bucket/upload1.test 5GB.file; aws s3 cp 5GB.file s3://$bucket/copy/5GB.file)  

2. Copy the file between S3 using a single command between locations. Record time to complete.  
  $ time aws s3 cp s3://$bucket/upload1.test s3://file s3://$bucket/copy/5GB-2.file)  

3. Use PUT COPY(copy-object) to move the file. Record time to complete.  
  $ time aws s3api --copy-source $bucket/upload1.test --bucket $bucket --key copy/5GB-3.file  

**Note**  
The first two commands required data to GET data from S3 back to the EC2 instance and then PUT the data back to S3 from the EC2 instance.  The third command copying data inside of S3 only.  This removes the consumption of EC2 instance network bandwidth making it much more efficient.  

## EFS Performance- Optimize IOPS

In this exercise we will demonstrate different methods of creating 1,024 files and compare the performance of each method.  

1. In the CLI for the instance, run this command to generate 1,024 zero byte files.
    Record time to complete.  

  $ directory=$(echo $(uuidgen)| grep -o ".\{6\}$")    
  $ mkdir -p /efs/tutorial/touch/${directory}  
  $ time for i in {1..1024}; do  
  $ touch /efs/tutorial/touch/${directory}/test-1.3-$i;  
  $ done;

2. Run this command to generate 1,024 zero by files using multiple threads.  Record time to complete.    
  $ directory=$(echo $(uuidgen)| grep -o ".\{6\}$")    
  $ mkdir -p /efs/tutorial/touch/${directory}    
  $ time seq 1 1024 | parallel --will-cite -j 128 touch /efs/tutorial/touch/${directory}/test-1.4-{}

3. Run this command to generate 1,024 zero by files in multiple directories using multiple threads. Record time to complete.  
  $ directory=$(echo $(uuidgen)| grep -o ".\{6\}$")   
  $ mkdir -p /efs/tutorial/touch/${directory}/{1..32}  
  $ time seq 1 32 | parallel --will-cite -j 32 touch /efs/tutorial/touch/${directory}/{}/test1.5{1..32}

**Note**  
The best way to leverage the distributed data storage design of Amazon EFS is to use multiple threads and inodes in parallel.  

## EFS Performance- I/O Sizes and Sync Frequency

In this exercise we will demonstrate how different I/O sizes and sync frequencies affects throughput to EFS.  

1. In the CLI for the instance, Write a 2GB file to EFS using 1MB block size and sync once after each file. Record time to complete.  
  $ time dd if=/dev/zero of=/efs/tutorial/dd/2G-dd-$(date +%Y%m%d%H%M%S.%3N) bs=1M count=2048 status=progress conv=fsync  

2. Write a 2 GB file to EFS using 16MB block size and sync once after each file. Record time to complete.  
  $ time dd if=/dev/zero of=/efs/tutorial/dd/2G-dd-$(date +%Y%m%d%H%M%S.%3N) bs=16M count=128 status=progress conv=fsync  

3. Write a 2GB file to EFS using 1MB block size and sync after each block. Record time to complete.  
  $ time dd if=/dev/zero of=/efs/tutorial/dd/2G-dd-$(date +%Y%m%d%H%M%S.%3N) bs=1M count=2048 status=progress oflag=sync  

4. Write a 2 GB file to EFS using 16MB block size and sync after each block.  Record time to complete.    
  $ time dd if=/dev/zero of=/efs/tutorial/dd/2G-dd-$(date +%Y%m%d%H%M%S.%3N) bs=16M count=128 status=progress oflag=sync  

**Note**  
Syncing after each block will dramatically decrease performance of the filesystem.  Best performance will be obtained by syncing after each file.  Block size has little impact to performance.  

## EFS Performance- Multi-threaded Performance

This exercise will demonstrate how multi-threaded access improves throughput and IOPS.  

1. Each command will write 2 GB of data to EFS using 1 MB block size.  
2. Write to EFS using 4 threads and sync after each block. Record time to complete.  
  $ time seq 0 3 | parallel --will-cite -j 4 dd if=/dev/zero of=/efs/tutorial/dd/2G-dd-$(date +%Y%m%d%H%M%S.%3N)-{} bs=1M count=512 oflag=sync

3. Write to EFS using 16 threads and sync after each block. Record time to complete.  
  $ time seq 0 15 | parallel --will-cite -j 16 dd if=/dev/zero of=/efs/tutorial/dd/2G-dd-$(date +%Y%m%d%H%M%S.%3N)-{} bs=1M count=128 oflag=sync  

**Note**
The distributed data storage design of EFS means that multi-threaded applications can drive substantial levels of aggregate throughput and IOPS.  
By parallelizing your writes to EFS by increasing the number of threads, you can increase the overall throughput and IOPS to EFS.  

## EFS Performance- Compare File Transfer Tools

In this section we will compare the performance of different file transfer utilities and EFS.  

1. Review the data to transfer.  2,000 files and 2 GB of data.  Record time to complete.  
  $ du -csh /ebs/tutorial/data-1m/  
  $ find /ebs/tutorial/data-1m/. -type f | wc -l

2. Transfer files from EBS to EFS using rsync  
  $ sudo su  
  $ sync && echo 3 > /proc/sys/vm/drop_caches  
  $ exit  
  $ time rsync -r /ebs/tutorial/data-1m/ /efs/tutorial/rsync/   

3. Transfer files from EBS to EFS using cp  
  $ sudo su  
  $ sync && echo 3 > /proc/sys/vm/drop_caches  
  $ exit  
  $ time cp -r /ebs/tutorial/data-1m/* /efs/tutorial/cp/  

4. Set the $threads variable to 4 threads per CPU  
  $ threads=$(($(nproc --all) * 4))  
  $ echo $threads  

5. Transfer files from EBS to EFS using fpsync  
$ sudo su  
  $ sync && echo 3 > /proc/sys/vm/drop_caches  
  $ exit  
  $ time fpsync -n ${threads} -v /ebs/tutorial/data-1m/ /efs/tutorial/fpsync/  

6. Transfer files from EBS to EFS using cp + GNU Parallel  
  $ sudo su  
  $ sync && echo 3 > /proc/sys/vm/drop_caches  
  $ exit  
  $ time find /ebs/tutorial/data-1m/. -type f | parallel --will-cite -j ${threads} cp {} /efs/tutorial/parallelcp   

**Note**  
Not all file transfer utilities are created equal. File systems are distributed across an unconstrained number of storage servers and this distributed data storage design means that multithreaded applications like fpsync, mcp, and GNU parallel can drive substantial levels of throughput and IOPS to EFS when compared to single-threaded applications.  

## EBS Performance Part 2
1. From the AWS console, click  **Services**  and select  **EC2.**  
2. Select  **Instances**  from the menu on the left.  
3. Select the instance named **Storage_Performance_Workshop**.  

  ![](/images/ebs_part1_2.png)
4. Click on **/dev/sdb** in the lower pane by Block devices.  

  ![](/images/ebs_part1_3.png)
5. In the pop up window, click the **EBS ID**.  

  ![](/images/ebs_part1_4.png)
6. Click on the **Monitoring** tab.  
7. There are two graphs of interest: Read Throughput and Burst Balance.  
   1. Read Throughput should be at 100 OPS now.  
   2. Burst Balance should be at 0%.  
8. In the CLI for the instance, Look at output of fio job to see current IOPs.  
  $ sudo screen -r
9. In the AWS console, click **Actions**, then select **Modify Volume**  
10. In the pop up window configure the following values:  

    Volume Type: Provisioned IOPS SSD (IO1)  
    Size: 100GB  
    Iops: 5000  

    ![](/images/ebs_part2_1.png)  
11. Click **Modify**.  
12. Click **Yes.**  
13. Click **Close.**  
14. Go back to your SSH session.  Check output of fio, you should see the increase in IOPS. ctrl-a d to exit screen.  
15. Verify larger volume is seen by instance  

  $ lsblk  

  ![](/images/ebs_part2_2.png)  
16. Resize the filesystem.  The increase in IOPs is available right away, but you would need to resize the filesystem to use the added capacity.  

  $ sudo umount /ebsperftest  
  $ sudo resize2fs /dev/nvme1n1  
  $ sudo mount /ebsperftest  

17. Verify filesystem is using 100 GB volume.

  $ df -h  

18. Run the following command to ensure FIO is running on the instance.  Output should be similar to below.  

  $ ps -ef | grep fio  

![](/images/ebs_part1_1.png)  
19. Allow fio to continue to run for several more minutes to allow graphs to update.  
20. Click on the **Monitoring** tab.  
21. Refresh graphs. Burst balance will no longer report any values due to the volume being IO1 now.  Read Throughput should be at 5,000 IOPS  

## Clean Up Resources

To ensurer you don't continue to be billed for services in your account from this workshop follow the steps below to remove all resources created ruing the workshop.  

1. In the CLI for the instance, remove objects from the S3 bucket.  
  $ aws configure set default.s3.max_concurrent_requests 20  
  $ aws s3 aws s3 rm s3://${bucket} --recursive  

2. From the AWS console, click  **Services**  and select  **CloudFormation.**  
3. Select **StoragePerformanceWorkshop**.  
4. Click **Delete**.  
5. Click **Delete stack**.  
6. It will take a few minutes to delete everything.  Refresh the page to see an updated status.   **StoragePerformanceWorkshop** will be removed from the list if everything has been deleted correctly.  
