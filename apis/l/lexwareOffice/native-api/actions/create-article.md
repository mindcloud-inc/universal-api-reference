# Create Article with Lexware Office

Creates a new article in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/articles`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Article](https://developers.lexware.io/docs/#articles-endpoint-create-an-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The article title. |
| `description` | body | `string` | no | The article description. |
| `type` | body | `string` | yes | The article type. |
| `articleNumber` | body | `string` | no | The article number. |
| `gtin` | body | `string` | no | The article GTIN. |
| `note` | body | `string` | no | An internal note for the article. |
| `unitName` | body | `string` | yes | The sales unit name. |
| `price.leadingPrice` | body | `string` | yes | Whether Lexware should treat NET or GROSS as the leading price. |
| `price.netPrice` | body | `number` | no | The net price when the leading price is NET. |
| `price.grossPrice` | body | `number` | no | The gross price when the leading price is GROSS. |
| `price.taxRate` | body | `number` | yes | The article tax rate. |
