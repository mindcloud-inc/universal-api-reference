# Create Job with Dribbble

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.dribbble.com/v2`
- **Official documentation:** [Create Job](https://developer.dribbble.com/v2/jobs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_name` | body | `string` | yes | — |
| `title` | body | `string` | yes | — |
| `location` | body | `string` | yes | — |
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
| `onsite_or_remote` | body | `boolean` | no | — |
| `onsite_only` | body | `boolean` | no | — |
| `remote_only` | body | `boolean` | no | — |
