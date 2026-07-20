# Generate Pydantic models from a document type with Affinda

Retrieves Pydantic models for an Affinda document type.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/document_types/:identifier/pydantic_models`
- **Base URL:** `https://api.us1.affinda.com`
- **Official documentation:** [Generate Pydantic models from a document type](https://docs.affinda.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Document type's identifier |
| `model_name` | query | `string` | no | Name for the Pydantic model |
