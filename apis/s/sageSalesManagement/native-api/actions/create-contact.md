# Create Contact with Sage Sales Management

Creates a contact in Sage Sales Management.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Create Contact](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | yes | Parent account ID |
| `lastName` | body | `string` | yes | Contact last name required by ForceManager when creating a contact. |
| `firstName` | body | `string` | yes | Contact first name required by ForceManager when creating a contact. |
