# Create Short Link with Once.to

Creates a new short link in Once.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/links`
- **Base URL:** `https://once.to/api/public/v1`
- **Official documentation:** [Create Short Link](https://docs.once.to/en/api/v1/endpoints/links-post/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | URL to redirect to. |
| `title` | body | `string` | no | Optional link title. |
