# Retrieve Multiple Reference Images with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/reference_images/bulk`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Retrieve Multiple Reference Images](https://api.gocanvas.com/api/v3/docs#retrieve-multiple-reference-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `number` | yes | Image IDs to retrieve, supplied as repeated ids[] parameters; maximum 10 per request. Send multiple values as a array. |
