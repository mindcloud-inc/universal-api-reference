# Parse CV Document with Mona AI

Parses a CV document in Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/parsing/parseCV`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Parse CV Document](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cvData` | body | `string` | no | Inline CV text or data to parse when no URL is used. |
| `cvUrl` | body | `string` | no | URL of the CV document to parse. |
| `parseOptions` | body | `object` | no | Parsing options object controlling extracted CV sections. |
| `permission` | body | `string` | yes | Mona permission string required by the CV parsing endpoint. |
