# Update Feed with Curator

Updates an existing feed in Curator.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/feeds/:FEED_ID`
- **Base URL:** `https://api.curator.io`
- **Official documentation:** [Update Feed](https://curator.io/docs/api/feeds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FEED_ID` | path | `string` | yes | ID of the feed to update. |
| `name` | body | `string` | yes | Updated feed name. |
