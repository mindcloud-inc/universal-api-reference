# Update User Profile Field with Rownd Data Privacy

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:user/data/fields/:field`
- **Base URL:** `https://api.rownd.io/applications/{appId}`
- **Official documentation:** [Update User Profile Field](https://docs.rownd.io/api-reference/user-profiles/app/update-field)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | path | `string` | yes | User-profile field name. |
| `user` | path | `string` | yes | Rownd user identifier. |
