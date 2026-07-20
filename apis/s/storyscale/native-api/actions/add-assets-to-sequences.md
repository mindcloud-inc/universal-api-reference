# Add Assets To Sequences with Storyscale

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/library/add-to-sequences`
- **Base URL:** `https://prodapi.storyscale.com/api`
- **Official documentation:** [Add Assets To Sequences](https://prodapi.storyscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assets` | body | `list<number>` | no | Asset IDs to add to the sequences. |
| `sequences` | body | `list<number>` | no | Sequence IDs to receive the selected assets. |
