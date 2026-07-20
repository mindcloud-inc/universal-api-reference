# Create Segment with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/segments`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Segment](https://docs.swipeone.com/en/articles/10545714-segments#h_247c00ee31)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | — |
| `name` | body | `string` | yes | — |
| `copyViewFrom` | body | `string` | yes | Source segment or view identifier to copy when creating a segment. |
| `criteria` | body | `object` | yes | — |
