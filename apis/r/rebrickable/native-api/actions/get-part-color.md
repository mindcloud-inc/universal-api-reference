# Get Part Color with Rebrickable

Retrieves a LEGO part color from Rebrickable.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/parts/:part_num/colors/:color_id/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [Get Part Color](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part_num` | path | `string` | yes | Rebrickable part number. |
| `color_id` | path | `number` | yes | Rebrickable color ID for the part/color combination. |
