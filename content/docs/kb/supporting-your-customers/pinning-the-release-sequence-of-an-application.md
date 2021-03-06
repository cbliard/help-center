---
date: "2017-11-01T00:00:00Z"
lastmod: "2017-11-01T00:00:00Z"
title: "Pinning the Release Sequence of an Application"
weight: "999999"
categories: [ "Supporting Your Customers" ]
index: "docs"
---

It is possible to pin the release sequence of a vendor application by creating or updating the file `/etc/replicated.conf` with property `"ReleaseSequence"` set to the numerical identifier of a release of the vendor application. This sequence number must correspond to a release that has been promoted to the channel to which the license is set.

For example:

```json
{
  "ReleaseSequence": 123
}
```

This file can be added before running the Replicated installation scripts to pin a release at install time. It is also possible to add or edit this file in a situation where Replicated is already running. In this case Replicated must be restarted for the changes to take effect. It is not possible to downgrade the vendor application using this method.
