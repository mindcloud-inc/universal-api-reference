# Assign User to Lead with Workiz

Assigns a user to a lead in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/assign/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Assign User to Lead](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `User` | body | `string` | yes | The user to assign. |
| `UUID` | body | `string` | yes | The lead UUID to assign. |
