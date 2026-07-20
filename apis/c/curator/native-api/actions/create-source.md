# Create Source with Curator

Creates a source for a feed in Curator.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sources`
- **Base URL:** `https://api.curator.io`
- **Official documentation:** [Create Source](https://curator.io/docs/api/sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feed_id` | body | `string` | yes | Feed to assign the source to. |
| `source_type` | body | `number` | yes | Curator source type ID. |
| `tag` | body | `string` | yes | Source tag or lookup value. |
