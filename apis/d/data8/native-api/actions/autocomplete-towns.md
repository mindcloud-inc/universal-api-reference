# Autocomplete Towns with Data8

Finds town name suggestions in Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/Location/AutoCompleteTowns.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Autocomplete Towns](https://docs.data-8.co.uk/web-services/geocoding/autocompletetowns)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `townName` | body | `string` | yes | The town name to autocomplete. |
| `options` | body | `object` | no | Optional settings that control location lookup behavior. |
