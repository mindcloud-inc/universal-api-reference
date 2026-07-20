# AutoGenerate a Schema with DocuPanda - Document Understanding

Creates a schema from documents in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/autogenerate`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [AutoGenerate a Schema](https://docs.docupipe.ai/reference/post_schema_autogenerate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | no | List of document IDs to use for schema generation. |
| `queries` | body | `list<string>` | no | List of example questions you would want to ask of your documents. |
| `schemaName` | body | `string` | yes | Name of the schema to be defined. For example rental contracts |
| `documentIds[]` | body | `array<string>` | no | List of document IDs to use for schema generation. |
| `dataset` | body | `string` | no | The dataset to which the documents belong. |
| `instructions` | body | `string` | no | Instructions on how to create the schema. |
| `guidelines` | body | `string` | no | Guidelines to apply to the schema to documents when standardizing. |
| `standardizeUsingSchema` | body | `boolean` | no | Whether to standardize the input documents using the newly created schema after generation.Note that standardizing documents costs credits just as if you had called the `/standardize` endpoint directly |
| `standardizationMode` | body | `object` | no | — |
