# Get Part with Rebrickable

Retrieves a LEGO part from Rebrickable by part number.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/parts/:part_num/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [Get Part](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part_num` | path | `string` | yes | Rebrickable part number to look up. |
