# Unassign User from Job with Workiz

Unassigns a user from a job in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/job/unassign/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Unassign User from Job](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `User` | body | `string` | yes | The user to unassign. |
| `UUID` | body | `string` | yes | The job UUID to unassign. |
