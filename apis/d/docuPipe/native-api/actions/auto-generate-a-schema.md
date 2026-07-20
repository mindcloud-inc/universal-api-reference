# AutoGenerate a Schema with DocuPipe

Generates a schema in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/schema/autogenerate`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [AutoGenerate a Schema](https://docs.docupipe.ai/reference/post_schema_autogenerate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schemaName` | body | `string` | no | Name of the schema to be defined. For example rental contracts |
| `documentIds[]` | body | `array<string>` | no | List of document IDs to use for schema generation. |
| `dataset` | body | `string` | no | The dataset to which the documents belong. |
| `instructions` | body | `string` | no | Instructions on how to create the schema. |
| `guidelines` | body | `string` | no | Guidelines to apply to the schema to documents when standardizing. |
| `standardizeUsingSchema` | body | `boolean` | no | Whether to standardize the input documents using the newly created schema after generation.Note that standardizing documents costs credits just as if you had called the `/standardize` endpoint directly |
| `standardizationMode` | body | `list` | no | *Advanced Feature* Mode of standardization to run, if standardizing using the schema. Accepted values: `default`, `sectionBased`, `spatial`. |
