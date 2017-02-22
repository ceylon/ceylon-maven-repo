# Ceylon Maven repo build of the distribution

This repository builds a Maven repository ready to be published locally, or to Maven Central

It is mostly generated with:

```bash
$ CEYLON_VERSION=1.3.2-SNAPSHOT
$ ceylon maven-export --for-import \
 ceylon.language/$CEYLON_VERSION \
 com.redhat.ceylon.compiler.java/$CEYLON_VERSION \
 com.redhat.ceylon.java.main/$CEYLON_VERSION \
 ceylon.runtime/$CEYLON_VERSION \
 ceylon.bootstrap/$CEYLON_VERSION \
 com.redhat.ceylon.tools/$CEYLON_VERSION
$ ceylon maven-export --out maven-sdk-repository --for-sdk-import \
 --rep ../ceylon-sdk/modules \
 ceylon.buffer/$CEYLON_VERSION \
 ceylon.collection/$CEYLON_VERSION \
 ceylon.dbc/$CEYLON_VERSION \
 ceylon.decimal/$CEYLON_VERSION \
 ceylon.file/$CEYLON_VERSION \
 ceylon.html/$CEYLON_VERSION \
 ceylon.http.client/$CEYLON_VERSION \
 ceylon.http.common/$CEYLON_VERSION \
 ceylon.http.server/$CEYLON_VERSION \
 ceylon.interop.java/$CEYLON_VERSION \
 ceylon.interop.persistence/$CEYLON_VERSION \
 ceylon.interop.spring/$CEYLON_VERSION \
 ceylon.io/$CEYLON_VERSION \
 ceylon.json/$CEYLON_VERSION \
 ceylon.locale/$CEYLON_VERSION \
 ceylon.logging/$CEYLON_VERSION \
 ceylon.math/$CEYLON_VERSION \
 ceylon.numeric/$CEYLON_VERSION \
 ceylon.process/$CEYLON_VERSION \
 ceylon.promise/$CEYLON_VERSION \
 ceylon.random/$CEYLON_VERSION \
 ceylon.regex/$CEYLON_VERSION \
 ceylon.time/$CEYLON_VERSION \
 ceylon.transaction/$CEYLON_VERSION \
 ceylon.unicode/$CEYLON_VERSION \
 ceylon.uri/$CEYLON_VERSION \
 ceylon.test/$CEYLON_VERSION \
 ceylon.whole/$CEYLON_VERSION
```

At this point you want to remove the current folders and take the new ones, BUT MAKE SURE
YOU ARE IN THE RIGHT FOLDER:

```
$ rm -rf ceylon* com.*
$ mv maven-repository/* .
$ mv maven-sdk-repository/* .
```
