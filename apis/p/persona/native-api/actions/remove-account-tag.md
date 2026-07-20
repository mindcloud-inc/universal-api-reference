# Remove Account Tag with Persona

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/[:account-id]/remove-tag`
- **Base URL:** `https://api.withpersona.com/api/v1`
- **Official documentation:** [Remove Account Tag](https://docs.withpersona.com/api-reference/accounts/remove-tag-from-an-account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account-id` | path | `string` | yes | Account ID |
| `meta.tag-name` | body | `string` | yes | Tag Name |
