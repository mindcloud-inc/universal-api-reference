# View a Contact with Freshsales Classic

Retrieves a contact from Freshsales Classic.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:id`
- **Base URL:** `https://{bundleAlias}/api`
- **Official documentation:** [View a Contact](https://developers.freshworks.com/crm/api/#view_a_contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The contact ID. |
| `include` | query | `string` | no | Optional related resources to embed in the contact response. |
