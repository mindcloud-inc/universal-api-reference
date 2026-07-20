# List budget requests with Platrum

Retrieves budget requests from Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/finplan/api/request/list`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [List budget requests](http://api.docs.platrum.ru/modules/finplan/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `finplans[]` | body | `array<string>` | no | Finplan periods to filter requests. |
