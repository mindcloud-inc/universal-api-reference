# Upsert User with SatisMeter

## Endpoint

- **Method:** `POST`
- **Path:** `/api/users`
- **Base URL:** `https://app.satismeter.com`
- **Official documentation:** [Upsert User](https://support.satismeter.com/hc/en-us/articles/6980457910163-Insert-Update-user-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project ID. |
| `userId` | body | `string` | yes | User ID used on your end to uniquely identify the user. |
| `traits.name` | body | `string` | no | Optional user name stored in SatisMeter traits. |
| `traits.email` | body | `string` | no | Optional user email stored in SatisMeter traits. |
| `traits.createdAt` | body | `date` | no | Optional user creation timestamp stored in SatisMeter traits. |
| `surveyDate` | body | `date` | no | Optional timestamp used to make the user eligible for an immediate survey display. |
