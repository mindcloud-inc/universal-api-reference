# Update Resource with Timekit

Updates an existing resource in Timekit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/resources/:id`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Update Resource](https://developers.timekit.io/reference/resources-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | First name of the resource. |
| `id` | path | `string` | yes | ID of the specific resource. |
| `last_name` | body | `string` | no | Last name of the resource. |
| `meta` | body | `object` | no | Metadata for the resource. |
| `password` | body | `string` | no | Password for the resource account. |
| `timezone` | body | `string` | no | Timezone of the resource. |
