# List Documents with iubenda

Retrieves documents from iubenda.

## Endpoint

- **Method:** `GET`
- **Path:** `/beta/documents`
- **Base URL:** `https://consent.iubenda.com`
- **Official documentation:** [List Documents](https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/#document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of documents to return. |
| `starting_after_identifier` | query | `string` | no | Cursor indicating after which identifier document results should be returned. |
