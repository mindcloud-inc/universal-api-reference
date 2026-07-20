# Add Numbers to Blacklist with Sempico Solutions SMS

## Endpoint

- **Method:** `POST`
- **Path:** `/black-list-add`
- **Base URL:** `https://restapi.sempico.solutions/v1`
- **Official documentation:** [Add Numbers to Blacklist](https://pypi.org/pypi/gatum-rest-py/json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numbers[]` | body | `array<string>` | yes | Phone numbers to add to the personal blacklist. |
