# Create User with Othership

Creates a new user in Othership.

## Endpoint

- **Method:** `POST`
- **Path:** `/Users`
- **Base URL:** `https://hwms-api.othership.com/api/v1/azure/scim`
- **Official documentation:** [Create User](https://www.ietf.org/rfc/rfc7644)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userName` | body | `string` | yes | The SCIM username, typically the user's work email. |
| `emails[].value` | body | `string` | no | The user's primary work email. |
| `displayName` | body | `string` | no | Display-friendly full name for the SCIM user. |
| `name.givenName` | body | `string` | no | The user's first name. |
| `name.familyName` | body | `string` | no | The user's last name. |
| `active` | body | `boolean` | no | Administrative status for the SCIM user. |
| `externalId` | body | `string` | no | Provisioning-domain identifier used to correlate the user across systems. |
