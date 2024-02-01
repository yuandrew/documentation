---
id: backgroundcheck-boilerplate-ssntrace-activity
title: Boilerplate Activity code
sidebar_label: Activity code
description: In the Temporal Python SDK programming model, an Activity is an function.
tags:
- go sdk
- code sample
- activity
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation/blob/main/sample-apps/python/backgroundcheck_boilerplate/activities/ssntraceactivity_dacx.py. -->

In the Temporal Python SDK programming model, an Activity is a function and can be used as an instance method of a class
You can use asynchronous, synchronous multithreaded, and synchronous multiprocess/other functions to define an Activity.

Below is an example of an Activity defined as a function.

<div class="copycode-notice-container"><a href="https://github.com/temporalio/documentation/blob/main/sample-apps/python/backgroundcheck_boilerplate/activities/ssntraceactivity_dacx.py">View the source code</a> in the context of the rest of the application code.</div>

```python
from temporalio import activity



@activity.defn
async def ssn_trace_activity(ssn) -> str:
    return "pass"
```