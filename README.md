# HA Tower CI/CD Project - Advanced Automation Homework
The playbooks and roles in this repository will:
- In QA Openstack environment:
  - Provision instances
  - Deploy 3 Tier App and smoketest
    - Cleanup instances if 3 Tier App deployment fails
    - If instances deploy successfully, move on to Production
- In Production AWS environment:
  - Provision instances in AWS
  - Deploy 3 Tier App and smoketest

## Basic Requirements
- An appropriate ansible.cfg in the project repository
- An ssh.cfg in the project repository that will leverage any jumphosts correctly
- Access to https://tower1.6678.example.opentlc.com/
- Tower should be configured with the appropriate inventories, credentials, projects, job templates, and workflow templates
  - https://tower1.6678.example.opentlc.com/ has been configured appropriately for you


##  In Tower
#### CI / CD Pipeline Workflow Job Template
- To run complete CI/CD pipeline workflow, run the `CI / CD Pipeline` Workflow Template

#### Provision QA Openstack Environment (including smoke test)
- To provision the QA Openstack environment and deploy the 3 tier app, execute the `Provision QA Environment and Deploy 3 Tier App - Openstack` Job Template

#### Cleanup QA Openstack Environment (including smoke test)
- To cleanup the QA Openstack 3 Tier App instances, execute the `Cleanup QA Instances - Openstack` Job Template

#### Provision AWS Production Environment
- To provision the AWS Production environment, execute the `Provision Prod Environment - AWS` Job Template

#### Deploy 3 Tier app to AWS Production Environment (including smoke test)
- To deploy the 3 Tier app to the AWS Production environment, execute the `Deploy 3 Tier App Prod Environment - AWS` Job Template


