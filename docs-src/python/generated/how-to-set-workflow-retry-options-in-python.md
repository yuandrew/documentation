---
id: how-to-set-workflow-retry-options-in-python
title: How to set Workflow Retry Options in Python
sidebar_label: Workflow Retry Options
description: Set the Retry Policy to either start_workflow() or execute_workflow().
tags:
- retry policy
- python sdk
- code sample
---

<!-- DO NOT EDIT THIS FILE DIRECTLY.
THIS FILE IS GENERATED from https://github.com/temporalio/documentation/blob/main/sample-apps/python/workflow_timeouts_retries/workflows_dacx.py. -->

Set the Retry Policy to either the [`start_workflow()`](https://python.temporal.io/temporalio.client.Client.html#start_workflow) or [`execute_workflow()`](https://python.temporal.io/temporalio.client.Client.html#execute_workflow) asynchronous methods.

<div class="copycode-notice-container"><a href="https://github.com/temporalio/documentation/blob/main/sample-apps/python/workflow_timeouts_retries/workflows_dacx.py">View the source code</a> in the context of the rest of the application code.</div>

```python
# ...
    handle = await client.execute_workflow(
        YourWorkflow.run,
        "your retry policy argument",
        id="your-workflow-id",
        task_queue="your-task-queue",
        retry_policy=RetryPolicy(maximum_interval=timedelta(seconds=2)),
    )
```