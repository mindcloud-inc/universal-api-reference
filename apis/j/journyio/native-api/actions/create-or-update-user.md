# Create or Update User with Journy.io

## Endpoint

- **Method:** `POST`
- **Path:** `/users/upsert`
- **Base URL:** `https://api.journy.io`
- **Official documentation:** [Create or Update User](https://developers.journy.io/#operation/upsertUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identification.email` | body | `string` | no | Email address of the user. |
| `identification.userId` | body | `string` | no | Unique identifier for the user in your database. |
| `properties` | body | `object` | no | User properties to create or update. |
