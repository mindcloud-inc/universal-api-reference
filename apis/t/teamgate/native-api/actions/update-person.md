# Update Person with Teamgate

Updates a person in Teamgate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/people/{{personId}}`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Update Person](https://developers.teamgate.com/#39163c34-52c9-440d-ba20-6067160c3812)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personId` | path | `string` | yes | Person ID to update. |
| `name` | body | `string` | no | Updated person name. |
| `starred` | body | `string` | no | Whether the person is starred. Use Teamgate values like yes or no. |
| `ownerId` | body | `string` | no | Updated owner user ID. |
| `sourceId` | body | `string` | no | Updated person source ID. |
| `industryId` | body | `string` | no | Updated person industry ID. |
| `tags` | body | `string` | no | Updated person tags. |
