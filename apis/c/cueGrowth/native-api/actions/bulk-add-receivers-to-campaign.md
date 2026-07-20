# Bulk Add Receivers To Campaign with CueGrowth

## Endpoint

- **Method:** `POST`
- **Path:** `/actions/bulk/add_receiver_to_campaign`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [Bulk Add Receivers To Campaign](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Array of receivers to add to the campaign. |
