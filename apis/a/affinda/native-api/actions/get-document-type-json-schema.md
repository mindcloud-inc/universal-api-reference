# Generate JSON schema from a document type with Affinda

Retrieves a JSON schema for an Affinda document type.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/document_types/:identifier/json_schema`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Generate JSON schema from a document type](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Document type's identifier |
| `title` | query | `string` | no | Title for the JSON schema |
