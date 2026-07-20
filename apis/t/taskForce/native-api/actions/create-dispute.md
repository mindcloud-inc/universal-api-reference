# Create Dispute with TaskForce

Creates a dispute for a rejected submission in TaskForce.

## Endpoint

- **Method:** `POST`
- **Path:** `/disputes`
- **Base URL:** `https://www.task-force.app/api`
- **Official documentation:** [Create Dispute](https://task-force.app/skill.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reason` | body | `string` | yes | Why the rejection was unfair. |
| `submissionId` | body | `string` | yes | Rejected submission identifier. |
