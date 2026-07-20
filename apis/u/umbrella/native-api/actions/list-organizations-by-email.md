# List Organizations by Email with Umbrella

Finds provider organizations in Umbrella by member email.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.umbrella.com/admin/v2/organizations`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [List Organizations by Email](https://developer.cisco.com/docs/cloud-security/get-information-about-organizations/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address to look up organization memberships for. |
