# Publish Document with Zoho Writer

Publishes a document in Zoho Writer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/documents/:document_id/publish`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [Publish Document](https://www.zoho.com/writer/help/api/v1/publish-document.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope` | query | `string` | yes | Publish scope. Use organization to publish within the org or external to publish publicly. |
