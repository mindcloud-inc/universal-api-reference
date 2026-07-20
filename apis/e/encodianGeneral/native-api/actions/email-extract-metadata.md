# Email Extract Metadata with Encodian - General

Extracts metadata from an email file in Encodian.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/General/GetEmailInfo`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Email Extract Metadata](https://support.encodian.com/hc/en-gb/articles/12237799140252)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileContent` | body | `string` | yes | Base64-encoded email file content. |
