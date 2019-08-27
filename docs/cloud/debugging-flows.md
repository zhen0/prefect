# Debugging Flows in Cloud

[[toc]]

### My flow is stuck in scheduled!

The most likely culprit when a flow is stuck in scheduled is the agent. Here are some steps
for debugging your agent:

[JOSH'S PART GOES HERE]

### My flow is stuck in submitted!

Having flows stuck in submitted most commonly indicates an issue with your execution cluster.
Here are are some steps for debugging issues in execution:

[JOSH YOU KNOW THIS BETTER THAN I DO]

### "Update failed: bad version"

Occasionally a task run will fail with the message "update failed: bad version." This is
due to Prefect Cloud's state locking mechanism, and actually means the system is working
as intended.
