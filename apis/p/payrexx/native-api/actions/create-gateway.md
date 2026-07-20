# Create Gateway with Payrexx

Creates a gateway in Payrexx.

## Endpoint

- **Method:** `POST`
- **Path:** `Gateway/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Create Gateway](https://developers.payrexx.com/reference/create-a-gateway)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | Amount of payment in cents. |
| `currency` | body | `string` | yes | Currency of payment (ISO code). |
| `purpose` | body | `string` | no | The purpose of the payment. |
| `referenceId` | body | `string` | no | An internal reference id used by your system. |
| `preAuthorization` | body | `boolean` | no | Whether charge payment manually at a later date (type authorization). |
| `reservation` | body | `boolean` | no | Whether charge payment manually at a later date (type reservation). |
