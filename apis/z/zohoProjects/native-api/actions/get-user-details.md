# Get User Details with Zoho Projects

Retrieves user details from Zoho Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/users/[:USERREF]`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Get User Details](https://projectsapi.zoho.com/api-docs#users_get-user-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `USERREF` | path | `string` | yes | Zoho Projects user ZPUID or email address. |
