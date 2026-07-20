# Search Group Numbers with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/group-number-search`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Search Group Numbers](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_group` | body | `number` | yes | Group ID to search. |
| `numbers[]` | body | `array<string>` | yes | Phone numbers to search for in the group. |
