# List Files with Woztell

Retrieves files from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [List Files](https://doc.woztell.com/open-api-reference/#query-apiViewer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include additionalIds, after, appId, before, fileIds, fileType, first, from, hideApiFiles, last, search, sizeMax, sizeMin, sortBy, and to. |
