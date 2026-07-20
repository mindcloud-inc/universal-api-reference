# Get pricing for all Routee Services with Routee

Retrieves pricing for all Routee services.

## Endpoint

- **Method:** `GET`
- **Path:** `/system/prices`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Get pricing for all Routee Services](https://docs.routee.net/reference/pricing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mcc` | query | `string` | no | The mcc to filter price results. |
| `mnc` | query | `string` | no | The mnc to filter price results. |
| `service` | query | `string` | no | The service to filter price results (possible values: Sms, Voice, TwoStep, Lookup, NumberValidator, Viber). |
