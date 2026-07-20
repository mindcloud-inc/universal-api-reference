# List Christmases with Is It Christmas?

## Endpoint

- **Method:** `GET`
- **Path:** `/api`
- **Base URL:** `https://isitchristmas.com`
- **Official documentation:** [List Christmases](https://github.com/isitchristmas/web/blob/master/api.js)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | ISO 3166-1 alpha-2 country code used for localized yes/no text. |
| `timezone` | query | `string` | no | IANA timezone name used to calculate Christmas in that zone. |
