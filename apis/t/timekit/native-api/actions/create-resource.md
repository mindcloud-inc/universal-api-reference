# Create Resource with Timekit

Creates a new resource in Timekit.

## Endpoint

- **Method:** `POST`
- **Path:** `/resources`
- **Base URL:** `https://api.timekit.io/v2`
- **Official documentation:** [Create Resource](https://developers.timekit.io/reference/resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `availability_constraints[]` | body | `array<object>` | no | Resource-level availability constraints. |
| `email` | body | `string` | no | Email of the resource. |
| `first_name` | body | `string` | no | First name of the resource. |
| `image` | body | `string` | no | Image URL for the resource. |
| `last_name` | body | `string` | no | Last name of the resource. |
| `meta` | body | `object` | no | Metadata for the resource. |
| `name` | body | `string` | yes | Set the resource name. |
| `password` | body | `string` | no | Password for the resource account. |
| `timezone` | body | `string` | yes | Timezone of the resource. |
