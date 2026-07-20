# Get Set with Rebrickable

Retrieves a LEGO set from Rebrickable by set number.

## Endpoint

- **Method:** `GET`
- **Path:** `/lego/sets/:set_num/`
- **Base URL:** `https://rebrickable.com/api/v3`
- **Official documentation:** [Get Set](https://rebrickable.com/api/v3/docs/?key=xxxxxxxxxx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `set_num` | path | `string` | yes | Rebrickable set number, such as 75192-1. |
