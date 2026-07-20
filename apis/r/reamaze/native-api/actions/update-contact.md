# Update Contact with Reamaze

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:identifier`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Update Contact](https://www.reamaze.com/api/put_contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Path parameter for identifier. |
| `contact` | body | `object` | no | Body payload field documented on https://www.reamaze.com/api/put_contacts. |
