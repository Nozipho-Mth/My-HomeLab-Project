# AWS Free Tier Setup

## 📌 Create Account
- Go to [AWS Free Tier](https://aws.amazon.com/free)
- Register with your email, credit card, and identity verification

## 👤 IAM Users and Groups
- Create IAM Users for better security
- Assign users to Groups based on **CIA**:
  - **Confidentiality**: Limit access to sensitive EC2 and billing
  - **Integrity**: Only certain users can change security groups
  - **Availability**: Full access to start/stop VMs

## 🔒 Enable MFA
- Use AWS console
- Link to Google Authenticator or Authy


⚠️ Importance of Stopping or Terminating Unused Instances
When using AWS Free Tier, it's crucial to manage your EC2 instances wisely to avoid unexpected charges.

💡 What You Need to Know
✅ AWS Free Tier gives you:

    -750 hours/month of free EC2 usage (t2.micro or t3.micro, depending on the region)
    -Valid for 12 months from the date you sign up
    -You may also get starter credits (e.g., $100–$300), depending on offers/promotions (usually valid for 30–90 days)

🚫 Leaving EC2 instances running:

    -Uses up your free-tier hours
    -You will be charged if you exceed the limits
    -Increases security risks if unattended services remain open

⏸️ Stopping vs. Terminating
  Stopping an instance:

    -Halts the VM, but you may still be charged for:
      -EBS (Elastic Block Store) storage
      -Elastic IPs (if allocated and not attached)
    -Keeps your data and configuration intact
  Terminating an instance:
        
    -Completely deletes the instance
    -You won’t be charged anymore
    -But ❗ you will lose all data unless it’s backed up (e.g., with snapshots or AMIs)

✅ Best Practices to Avoid Unwanted Costs
    🛑 Stop instances when not in use
    🗑️ Terminate instances when you’re done and have saved your work
    💬 Set up Cost Budgets and Alarms in AWS Billing to get notified when:
        
        -You reach a defined usage limit
        -You’re approaching or exceeding your Free Tier limits
