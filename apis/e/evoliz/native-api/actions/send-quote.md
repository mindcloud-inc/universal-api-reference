# Send Quote with Evoliz

Sends a quote by email from Evoliz.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/quotes/:quoteid/send`
- **Base URL:** `https://www.evoliz.io`
- **Official documentation:** [Send Quote](https://evoliz.io/documentation#tag/Quote/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1quotes~1%7Bquoteid%7D~1send/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quoteid` | path | `number` | yes | The Evoliz quote ID. |
