These Resource Agent files need to be copied in to /usr/lib/ocf/resource.d/heartbeat/

## Examples.

* scriptexecutor examples.
  * cib configuration with a specific user :
```
primitive test scriptexecutor \
        params state="/home/testuser/test.sh" USER=testuser \
        op start timeout=600 interval=0 \
        meta target-role=Started
```

*  * cib configuration with root user : 
```
primitive test scriptexecutor \
        params state="/root/test.sh" \
        op start timeout=600 interval=0 \
        meta target-role=Started
```
