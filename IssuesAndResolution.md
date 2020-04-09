### Issue#1
```
Insufficient Permission: Request had insufficient authentication scopes.

When I ssh to the vm, I want to run gcloud command, but shows error like this:

yclin1822@guruvm:~$ gcloud compute instances list

ERROR: (gcloud.compute.instances.list) Some requests did not succeed: - Insufficient Permission: Request had insufficient authentication scopes.

How can I solve it?
```
#### Resolution:
```
Reason:
During the instance creation in "Access scopes" you used the Default option need to choose the "Allow full access to all Cloud APis" option.

Once you already created do the steps:

stop the VM instance
click in Edit , next in API access scopes select "Allow full access to all Cloud APis" and click in save
Start instance and check please
Hope it helps.
```