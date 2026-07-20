# Find Location with Data8

Finds location details in Data8 by postcode.

## Endpoint

- **Method:** `POST`
- **Path:** `/Location/FindLocation.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Location](https://docs.data-8.co.uk/web-services/geocoding/findlocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `postcode` | body | `string` | yes | The postcode to get the location of. |
| `options` | body | `object` | no | Optional settings that control location lookup behavior. |
