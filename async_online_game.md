![image](https://github.com/ronitwilson/aws_arch_study/assets/9934360/b53fa40c-652c-4b32-8c3e-83140eeda253)

# In  Route 53 they have used routing rules
* Something like load balancing ?
* elastic load balancer vs route 53 load balancing
  * https://stackoverflow.com/questions/57321793/elastic-load-balancer-elb-and-route-53-in-aws
  * Both Route53 and ELB are used to distribute the network traffic. These AWS services appear similar but there are minor differences between them.
  * ELB distributes traffic among Multiple Availability Zone but not to multiple Regions. Route53 can distribute traffic among multiple Regions. In short, ELBs are intended to load balance across EC2 instances in a single region whereas DNS load-balancing (Route53) is intended to help balance traffic across regions.
  * Both Route53 and ELB perform health check and route traffic to only healthy resources. Route53 weighted routing has health checks and removes unhealthy targets from its list. **However, DNS is cached so unhealthy targets will still be in the visitors cache for some time**. On the other hand, ELB is not cached and will remove unhealthy targets from the target group immediately.
# There are 2 AZ for high availability
# The webservers are not business logic, they are the entry point to the applications
 * Helps to handle ddos attacks
# Note there is Redis primary and secondary db's, similar they have aurora main and  replicas
# SNS has integration to the iphone and android api's
