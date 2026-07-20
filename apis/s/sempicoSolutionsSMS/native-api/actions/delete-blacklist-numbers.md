# Delete Blacklist Numbers with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/black-list-delete`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Delete Blacklist Numbers](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers[]` | body | `array<string>` | yes | Phone numbers to delete from the personal blacklist. |
