# Archive Upload with Printify

Archives an uploaded image in Printify.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/:image_id/archive.json`
- **Base URL:** `https://api.printify.com/v1/`
- **Official documentation:** [Archive Upload](https://developers.printify.com/API-Doc-RREdits.html/1000)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `image_id` | path | `string` | yes | Printify uploaded image id. |
