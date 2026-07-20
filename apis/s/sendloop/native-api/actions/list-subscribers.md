# List Subscribers with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriber.browse/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [List Subscribers](https://chmyos.notion.site/List-Subscribers-0a8cd681380d428cbe0f217dc151d89a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ListID` | body | `number` | yes | ID of the target list to get subscribers |
| `SegmentID` | body | `number` | no | ID of the segment in the target list to get subscribers |
| `StartIndex` | body | `number` | no | Page index to get subscribers from; each call returns 100 records |
