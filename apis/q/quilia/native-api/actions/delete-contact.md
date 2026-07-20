# Delete Contact with Quilia

## Endpoint

- **Method:** `DELETE`
- **Path:** `contacts/:id`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Delete Contact](https://api.quilia.dev/v2#tag/contacts/DELETE/contacts/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the contact to delete |
| `type` | query | `list<string>` | yes | The type of contact to delete Accepted values: `company`, `people`. |
