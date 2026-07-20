# Assign User to Job with Workiz

Assigns a user to a job in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/job/assign/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Assign User to Job](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `User` | body | `string` | yes | The user to assign. |
| `UUID` | body | `string` | yes | The job UUID to assign. |
