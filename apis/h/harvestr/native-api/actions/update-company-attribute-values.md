# Update Company Attribute Values with Harvestr.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/company/{id}/attribute/{attributeId}`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Update Company Attribute Values](https://developers.harvestr.io/api/update-attribute-values-from-a-company/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `attributeId` | path | `string` | yes | ID of the attribute to retrieve for the company |
| `textValue` | body | `string` | no | Required for TEXT attribute |
| `numericValue` | body | `number` | no | Required for NUMERIC attribute |
| `booleanValue` | body | `boolean` | no | Required for BOOLEAN attribute |
| `dateValue` | body | `string` | no | Required for DATE attribute |
| `urlValue` | body | `string` | no | Required for URL attribute |
| `ratingValue` | body | `string` | no | Required for RATING attribute |
