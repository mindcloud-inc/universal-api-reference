# List Jobs with Toast

Retrieves labor jobs for the connected restaurant, optionally limited to specific identifiers.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/jobs`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [List Jobs](https://doc.toasttab.com/openapi/labor/operation/jobsGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobIds` | query | `string` | no | One or more Toast GUIDs or external job identifiers, with a maximum of 100. Send multiple values as a array. |
