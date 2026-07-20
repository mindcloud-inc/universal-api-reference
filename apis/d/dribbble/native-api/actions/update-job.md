# Update Job with Dribbble

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/:id`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Update Job](https://developer.dribbble.com/v2/jobs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Dribbble job ID. |
| `organization_name` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `location` | body | `string` | no | — |
| `link_to_apply` | body | `string` | yes | — |
| `description` | body | `string` | yes | — |
| `active` | body | `boolean` | no | — |
| `team` | body | `string` | no | — |
| `category` | body | `list` | no | Accepted values: `Animator`, `Art Director`, `Brand Designer`, `Creative Director`, `Front-end Developer`, `Graphic Designer`, `Illustrator`, `Interaction Designer`, `Mobile Designer`, `Mobile Developer`, `Motion Designer`, `Other`, `Product Designer`, `UI/UX Designer`, `Web Designer`. |
| `role_type` | body | `list` | no | Accepted values: `contract`, `freelance`, `full-time`, `part-time`. |
| `website` | body | `string` | no | — |
| `twitter` | body | `string` | no | — |
| `instagram` | body | `string` | no | — |
| `facebook` | body | `string` | no | — |
