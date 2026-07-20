# Get User with Ziflow

Retrieves a user from Ziflow by ID or email.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:identifier`
- **Base URL:** `https://api.ziflow.io/v1`
- **Official documentation:** [Get User](https://api-docs.ziflow.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | User identifier (ID or email). |
