# Update Incident with Reamaze

## Endpoint

- **Method:** `PUT`
- **Path:** `/incidents/:identifier`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Update Incident](https://www.reamaze.com/api/put_incident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Path parameter for identifier. |
| `incident` | body | `object` | no | Body payload field documented on https://www.reamaze.com/api/put_incident. |
