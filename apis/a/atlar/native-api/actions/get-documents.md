# Get documents with Atlar

Retrieves documents from Atlar by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounting/v2beta/documents:batch`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Get documents](https://docs.atlar.com/reference/get-accounting-v2beta-documents-batch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids[]` | query | `array<string>` | yes |
