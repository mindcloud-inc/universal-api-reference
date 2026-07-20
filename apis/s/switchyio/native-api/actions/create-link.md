# Create Link with Switchy.io

Creates a new link in Switchy.io.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.switchy.io/v1/links/create`
- **Base URL:** `https://graphql.switchy.io`
- **Official documentation:** [Create Link](https://developers.switchy.io/docs/guides/how-to-create-a-link)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | yes |
| `domain` | body | `string` | yes |
| `id` | body | `string` | yes |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
