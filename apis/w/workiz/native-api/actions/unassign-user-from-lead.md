# Unassign User from Lead with Workiz

Unassigns a user from a lead in Workiz.

## Endpoint

- **Method:** `POST`
- **Path:** `/lead/unassign/`
- **Base URL:** `https://api.workiz.com/api/v1/{apiKey}`
- **Official documentation:** [Unassign User from Lead](https://developer.workiz.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `User` | body | `string` | yes | The user to unassign. |
| `UUID` | body | `string` | yes | The lead UUID to unassign. |
