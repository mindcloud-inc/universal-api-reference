# Get User with HubSpot

Retrieves a user from HubSpot by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `crm/v3/objects/users/:userId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Get User](https://developers.hubspot.com/docs/api-reference/crm-users-v3/basic/get-crm-v3-objects-users-userId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The ID of the user to retrieve. |
| `idProperty` | query | `list` | no | Which unique user identifier the `userId` value represents. Accepted values: `hs_email`, `hs_internal_user_id`. |
| `properties` | query | `string` | no | Comma-separated list of properties to return. Send multiple values as a string separated by `,`. |
| `propertiesWithHistory` | query | `string` | no | Comma-separated list of properties to return with value history. Send multiple values as a string separated by `,`. |
| `associations` | query | `string` | no | Comma-separated list of object associations to retrieve with the user. Send multiple values as a string separated by `,`. |
| `archived` | query | `boolean` | no | Whether to return archived records. |
