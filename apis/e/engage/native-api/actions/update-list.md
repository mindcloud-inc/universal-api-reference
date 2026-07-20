# Update List with Engage

Updates an existing list in Engage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:id`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Update List](https://docs.engage.so/en-us/a/62bbdd2e5bfea4dca4834045-lists#update-a-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Engage list ID. |
| `title` | body | `string` | no | List title. |
| `description` | body | `string` | no | List description. |
| `redirect_url` | body | `string` | no | URL to redirect users to after subscription. |
| `double_optin` | body | `boolean` | no | Whether subscribers should confirm their subscription by email. |
