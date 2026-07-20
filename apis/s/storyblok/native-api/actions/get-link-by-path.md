# Get Link by UUID with Storyblok

Retrieves a Storyblok link by UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/links/:linkId`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Get Link by UUID](https://www.storyblok.com/docs/api/content-delivery/v2/links/the-link-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | The Storyblok link UUID. |
| `version` | query | `string` | no | Whether to read draft or published content. |
