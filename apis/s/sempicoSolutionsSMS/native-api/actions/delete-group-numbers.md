# Delete Group Numbers with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/group-number-delete`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Delete Group Numbers](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_group` | body | `number` | yes | Group ID to remove numbers from. |
| `numbers[]` | body | `array<string>` | yes | Phone numbers to remove from the group. |
