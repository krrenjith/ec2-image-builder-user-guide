# EC2 Image Builder User Guide

-----
*****Copyright &copy; 2020 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is EC2 Image Builder?](what-is-image-builder.md)
+ [How EC2 Image Builder works](how-image-builder-works.md)
+ [Get started with EC2 Image Builder](getting-started-image-builder.md)
   + [Prerequisites](image-builder-setting-up.md)
   + [Access EC2 Image Builder](image-builder-accessing-prereq.md)
   + [Create an image pipeline using the EC2 Image Builder console wizard](start-build-image-pipeline.md)
   + [Create a container image pipeline using the EC2 Image Builder console wizard](start-build-container-pipeline.md)
+ [EC2 Image Builder component manager](image-builder-component-manager.md)
   + [Use documents in EC2 Image Builder](image-builder-application-documents.md)
   + [Develop Image Builder components locally](image-builder-component-manager-local.md)
   + [Use looping constructs in the AWSTOE application](image-builder-looping-constructs.md)
   + [Define and reference variables in the AWSTOE application](image-builder-component-manager-user-defined-variables.md)
   + [Component manager supported action modules](image-builder-action-modules.md)
   + [Verify the signature of the AWSTOE installation download](awstoe-verify-sig.md)
   + [EC2 Image Builder STIG components](image-builder-stig.md)
+ [Manage EC2 Image Builder resources](manage-resources.md)
   + [Manage components with AWSTOE](manage-components.md)
      + [List and view component details](component-details.md)
      + [Create a component using the Image Builder console](create-component-console.md)
      + [Create a component (AWS CLI)](create-components-cli.md)
   + [Manage recipes](manage-recipes.md)
      + [List and view image recipe details](image-recipe-details.md)
      + [List and view container recipe details](container-recipe-details.md)
      + [Create image recipes and versions](create-image-recipes.md)
      + [Create container recipes and versions](create-container-recipes.md)
   + [Manage EC2 Image Builder images](manage-images.md)
      + [List and view image details](image-details.md)
      + [Create images](create-images.md)
   + [Manage EC2 Image Builder infrastructure configuration](manage-infra-config.md)
      + [List and view infrastructure configuration details](infra-config-details.md)
      + [Create and update infrastructure configurations](create-infra-config.md)
   + [Manage EC2 Image Builder distribution settings](manage-distribution-settings.md)
      + [List and view distribution settings detail](distribution-settings-detail.md)
      + [Create and update distribution settings](create-distribution-settings.md)
   + [Share EC2 Image Builder resources](manage-shared-resources.md)
   + [Tag EC2 Image Builder resources](tag-resources.md)
   + [Delete EC2 Image Builder resources](delete-resources.md)
+ [Manage EC2 Image Builder pipelines using the console](manage-pipelines.md)
   + [List and view pipeline details](pipeline-details.md)
   + [Create and update container image pipelines](container-image-pipelines.md)
      + [Create a container image pipeline (AWS CLI)](cli-create-container-pipeline.md)
      + [Update a container image pipeline (console)](update-container-pipelines-console.md)
      + [Update container image pipelines (AWS CLI)](cli-update-container-pipeline.md)
      + [Run your container image pipeline](container-pipelines-run.md)
   + [Create and update AMI image pipelines](ami-image-pipelines.md)
      + [Create an AMI image pipeline (AWS CLI)](cli-create-image-pipeline.md)
      + [Update AMI image pipelines (console)](update-image-pipelines-console.md)
      + [Update AMI image pipelines (AWS CLI)](cli-update-image-pipeline.md)
      + [Run your AMI image pipeline](pipelines-run.md)
   + [Use cron expressions in EC2 Image Builder](cron-expressions.md)
+ [Security in EC2 Image Builder](image-builder-security.md)
   + [EC2 Image Builder and interface VPC endpoints (AWS PrivateLink)](vpc-interface-endpoints.md)
   + [Data protection in EC2 Image Builder](data-protection.md)
   + [Identity and Access Management for EC2 Image Builder](security-iam.md)
      + [How EC2 Image Builder works with IAM](security_iam_service-with-iam.md)
      + [EC2 Image Builder identity-based policy examples](security_iam_id-based-policy-examples.md)
      + [EC2 Image Builder resource-based policy examples](security_iam_resource-based-policy-examples.md)
      + [Using service-linked roles for EC2 Image Builder](image-builder-service-linked-role.md)
      + [Troubleshooting EC2 Image Builder identity and access](security_iam_troubleshoot.md)
   + [Compliance validation for EC2 Image Builder](compliance.md)
   + [Resilience in EC2 Image Builder](disaster-recovery-resiliency.md)
   + [Infrastructure security in EC2 Image Builder](infrastructure-security.md)
   + [Patch Management in EC2 Image Builder](vulnerability-analysis-and-management.md)
   + [Security best practices for EC2 Image Builder](security-best-practices.md)
+ [Troubleshoot EC2 Image Builder](image-builder-troubleshooting.md)
+ [Document History for EC2 Image Builder User Guide](doc-history.md)
+ [AWS glossary](glossary.md)