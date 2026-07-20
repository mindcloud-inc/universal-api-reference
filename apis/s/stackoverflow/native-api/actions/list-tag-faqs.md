# List Tag FAQs with Stackoverflow

Retrieves tag FAQs from Stackoverflow.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/[:tags]/faq`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [List Tag FAQs](https://api.stackexchange.com/docs/faqs-by-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | path | `string` | yes | Semicolon-delimited tag names. |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
