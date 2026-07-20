# Update Source with Curator

Updates an existing source in Curator.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sources/:SOURCE_ID`
- **Base URL:** `https://api.curator.io`
- **Official documentation:** [Update Source](https://curator.io/docs/api/sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `SOURCE_ID` | path | `string` | yes | ID of the source to update. |
| `name` | body | `string` | yes | Updated source name. |
| `tag` | body | `string` | yes | Runtime-required source tag value for the updated source. |
