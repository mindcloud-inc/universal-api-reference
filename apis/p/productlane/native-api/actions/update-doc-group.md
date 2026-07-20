# Update Doc Group with Productlane

Updates a doc group in your Productlane help center.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/docs/groups/{id}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Update Doc Group](https://productlane.mintlify.dev/docs/api/docs/update-doc-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Doc group ID. |
| `name` | body | `string` | no | Updated docs group name. |
| `order` | body | `number` | no | Display order for the group. |
