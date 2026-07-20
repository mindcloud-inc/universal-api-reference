# List Tags with The Guardian

Finds matching tags in The Guardian.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://content.guardianapis.com`
- **Official documentation:** [List Tags](https://raw.githubusercontent.com/guardian/open-platform-site/gh-pages/documentation/md/tag.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Return tags containing exactly this free text. |
| `reference` | query | `string` | no | Filter tags by reference value. |
| `reference-type` | query | `string` | no | Filter tags by reference type. |
| `section` | query | `string` | no | Filter tags to one or more sections. |
| `show-references` | query | `string` | no | Comma-separated reference groups to include in each tag result. |
| `type` | query | `string` | no | Filter tags by type. |
| `web-title` | query | `string` | no | Return tags whose web title starts with this prefix. |
