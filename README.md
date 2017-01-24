# Ceylon Maven repo build of the distribution

This repository builds a Maven repository ready to be published locally, or to Maven Central

It is mostly generated with:

```bash
$ ceylon maven-export --for-import ceylon.language/1.3.2-SNAPSHOT \
 com.redhat.ceylon.compiler.java/1.3.2-SNAPSHOT \
 com.redhat.ceylon.java.main/1.3.2-SNAPSHOT \
 ceylon.runtime/1.3.2-SNAPSHOT \
 ceylon.bootstrap/1.3.2-SNAPSHOT \
 com.redhat.ceylon.tools/1.3.2-SNAPSHOT
```
