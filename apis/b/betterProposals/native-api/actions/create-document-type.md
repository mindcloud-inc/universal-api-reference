# Create Document Type with Better Proposals

Creates a document type in Better Proposals.

## Endpoint

- **Method:** `POST`
- **Path:** `/doctype/create`
- **Base URL:** `https://api.betterproposals.io`
- **Official documentation:** [Create Document Type](https://betterproposals.io/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TypeName` | body | `string` | yes | Document type name. |
| `TypeColour` | body | `string` | no | Colour for the new document type. Default is #01A3EF. |
