# Update Link with Switchy.io

Updates an existing link in Switchy.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `https://api.switchy.io/v1/links/by-domain/:domain/:id`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Update Link](https://developers.switchy.io/docs/guides/how-to-update-a-link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `domain` | path | `string` | yes |
| `id` | path | `string` | yes |
| `url` | body | `string` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
