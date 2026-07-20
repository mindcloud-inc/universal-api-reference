# List Glossaries with HappyScribe

Retrieves glossaries from HappyScribe.

## Endpoint

- **Method:** `GET`
- **Path:** `/glossaries`
- **Base URL:** `https://www.happyscribe.com/api/v1`
- **Official documentation:** [List Glossaries](https://dev.happyscribe.com/sections/product/#glossaries-list-glossaries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Workspace organization ID required by HappyScribe for listing glossaries. |
