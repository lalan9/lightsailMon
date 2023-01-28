# Lightsail Monitor
An AWS Lightsail monitor service

### How to use
```yaml
LogLevel: warning # Log level: debug, info, warn, error, fatal, panic
Internal: 300 # Time to check the node connection (unit: second)
Timeout: 15 # Timeout for the tcp request (unit: second)
Accounts:
  - AccessKeyID: YOUR_AWS_AccessKeyID
    SecretAccessKey: YOUR_AWS_SecretAccessKey
    Regions:
      - Name: ap-northeast-1 # AWS service endpoints, check https://docs.aws.amazon.com/general/latest/gr/rande.html for help
        Nodes:
          - Address: node1.test.com # The node domain
            Port: 8080 # The node port
      - Name: ap-southeast-1 # AWS service endpoints, check https://docs.aws.amazon.com/general/latest/gr/rande.html for help
        Nodes:
          - Address: node2.test.com # The node domain
            Port: 8080 # The node port
#  - AccessKeyID: YOUR_AWS_AccessKeyID_2
#    SecretAccessKey: YOUR_AWS_SecretAccessKey_2
#    Regions:
#      - Name: ap-northeast-1
#        Nodes:
#          - Address: node3.test.com
#            Port: 8080
#      - Name: ap-southeast-1
#        Nodes:
#          - Address: node4.test.com
#            Port: 8080

```