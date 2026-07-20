# Get Minifig with Rebrickable

Retrieves a LEGO minifig from Rebrickable by set number.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/minifigs/:set_num/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [Get Minifig](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `set_num` | path | `string` | yes | Rebrickable minifig set number, such as fig-000001. |
