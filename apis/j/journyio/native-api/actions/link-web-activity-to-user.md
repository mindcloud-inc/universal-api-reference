# Link Web Activity to User with Journy.io

## Endpoint

- **Method:** `POST`
- **Path:** `/link`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Link Web Activity to User](https://developers.journy.io/#operation/link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | body | `string` | yes | Value of the __journey cookie to link. |
| `identification.email` | body | `string` | no | Email address of the user. |
| `identification.userId` | body | `string` | no | Unique identifier for the user in your database. |
