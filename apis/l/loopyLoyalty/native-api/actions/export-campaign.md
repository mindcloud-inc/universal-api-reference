# Export Campaign with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/export/:id`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Export Campaign](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_exportCampaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign ID. |
| `timezone` | body | `string` | no | Timezone string in IANA timezone format. |
| `segment` | body | `string` | no | Segment to export. |
