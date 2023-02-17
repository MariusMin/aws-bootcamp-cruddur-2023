# Week 0 — Billing and Architecture
## Adding explanation how this week went.

I have learned a lot of new tools. Watched all of the pre-requisite vidoes. It was quite hard not having all the basics. Should have spend more time during the official start

I work AWS partner company so I'm quite familiar with well-architected tool as we perform them to our clients. So at least this part I could skip and concentrate more on the github and gitpod which for me are unfamiliar as we use the Atlasian product which is Bitbucket.

### Installing AWS CLI

I did watch the whole video quite some time without actually completing it to the end. At some point I always did something wrong and incomplete and it actually took me some twime to figure and complete it. I did do it via gitpod so after watching the Updating Your Journal in Gitpod I understood that for this part i do not have to provide proof.
But ok. Let's go what we did is install CLI in gitpod.

 $ curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

after the run did export access and secret keys. They are storred in GitPod. Also as I'm From Europe i'm using eu-central-1 region.
I've update gitpod.yml file  in gitpod jaml file so it would install it every time we start the pod.



```sh
tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
      
      
   ```
   So we did also setup billing allarms and notifications as instructed. Strange that same evening i received an allert about 1$ bill. But signed into console and i saw that predicted bill for now said $1.32. Went there and also deleted some old notifications, old billing alarms on the same note did some cleanup of not needed S3 buckets.
   
### create a Billing Alarm

[Image of the Alarm Configuration](asets/alarmconfig.png)

### created Budget from CLI 
Have set a budget of 19$ just I know that i will go definetly over 15. I use S3 for storing of some items there.
[Image of the budget](asets/budgedaws.png)



### Logical Architecture
[Logical Architecture from lucid charts](asets/lucid-chart.png)
### Napkin design
