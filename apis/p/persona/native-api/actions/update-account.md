# Update Account with Persona

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts/[:account-id]`
- **Base URL:** `https://api.withpersona.com/api/v1`
- **Official documentation:** [Update Account](https://docs.withpersona.com/api-reference/accounts/update-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `string` | yes | Account ID |
| `data.attributes.reference-id` | body | `string` | no | Reference ID |
