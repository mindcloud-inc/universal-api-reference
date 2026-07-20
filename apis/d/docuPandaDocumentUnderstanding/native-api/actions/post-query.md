# Query Standardizations with DocuPanda - Document Understanding

Creates a natural-language standardization query in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/query`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Query Standardizations](https://docs.docupipe.ai/reference/post_query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | body | `string` | no | Name of the dataset to which the document belongs If empty, the query will run on all documents |
| `limit` | body | `number` | no | Maximum number of documents to return. If not specified will default to 100 |
| `query` | body | `string` | yes | Free language text explaining what documents you're after. if the text is empty |
| `schemaId` | body | `string` | yes | Unique identifier of the schema. |
