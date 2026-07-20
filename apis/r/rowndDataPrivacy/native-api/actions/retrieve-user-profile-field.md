# Retrieve User Profile Field with Rownd Data Privacy

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user/data/fields/:field`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Retrieve User Profile Field](https://docs.rownd.io/api-reference/user-profiles/app/retrieve-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | path | `string` | yes | User-profile field name. |
| `user` | path | `string` | yes | Rownd user identifier. |
