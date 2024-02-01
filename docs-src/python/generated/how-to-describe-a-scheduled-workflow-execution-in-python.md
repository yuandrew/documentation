---
id: how-to-describe-a-scheduled-workflow-execution-in-python
title: How to describe a Scheduled Workflow Execution in Python
sidebar_label: Describe a Scheduled Workflow Execution
description: Use the `describe()` asynchronous method on the Schedule Handler.
tags:
- scheduled workflow execution
- schedules
- python sdk
- code sample
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation/blob/main/sample-apps/python/schedule_your_workflow/describe_schedule_dacx.py. -->

To describe a Scheduled Workflow Execution in Python, use the [describe()](https://python.temporal.io/temporalio.client.ScheduleHandle.html#delete) asynchronous method on the Schedule Handle.
You can get a complete list of the attributes of the Scheduled Workflow Execution from the [ScheduleDescription](https://python.temporal.io/temporalio.client.ScheduleDescription.html) class.

<div class="copycode-notice-container"><a href="https://github.com/temporalio/documentation/blob/main/sample-apps/python/schedule_your_workflow/describe_schedule_dacx.py">View the source code</a> in the context of the rest of the application code.</div>

```python
# ...
async def main():
    client = await Client.connect("localhost:7233")
    handle = client.get_schedule_handle(
        "workflow-schedule-id",
    )

    desc = await handle.describe()

    print(f"Returns the note: {desc.schedule.state.note}")
```