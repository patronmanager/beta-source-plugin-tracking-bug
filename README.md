# Repro steps
```shell
sfdx force:org:create --setdefaultusername -f config/project-scratch-def.json
sfdx force:source:beta:push
```

Actual: push reports that the 2 Apex classes were deployed when in fact they were not; subsequent pushes omit those classes from push

Expected: nothing is pushed due to deployment error and subsequent push attempts try to push all unpushed metadata