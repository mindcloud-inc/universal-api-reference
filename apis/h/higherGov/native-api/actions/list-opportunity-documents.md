# List Opportunity Documents with HigherGov

Retrieves opportunity documents from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/document/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List Opportunity Documents](https://www.highergov.com/api-external/docs/#/api-external/api_external_document_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `related_key` | query | `string` | yes | Document key from the Opportunity endpoint document_path field |
