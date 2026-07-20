# Register Sub-Account with LinkedCamp

## Endpoint

- **Method:** `POST`
- **Path:** `/users/register`
- **Base URL:** `https://api.linkedcamp.com`
- **Official documentation:** [Register Sub-Account](https://api.linkedcamp.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Sub-account user name. |
| `email` | body | `string` | yes | Sub-account email address. |
| `planId` | body | `string` | yes | LinkedCamp plan identifier. |
