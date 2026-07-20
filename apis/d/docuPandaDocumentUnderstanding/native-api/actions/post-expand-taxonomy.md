# Expand Class Taxonomy with DocuPanda - Document Understanding

Creates class taxonomy expansions in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/class/expand`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Expand Class Taxonomy](https://docs.docupipe.ai/openapi/docupanda.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documentIds` | body | `list<string>` | yes | List of document IDs to be processed. |
| `instructions` | body | `string` | no | Instructions for the AI on how to expand the taxonomy. |
