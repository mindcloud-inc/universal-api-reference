# Create Customer with Baremetrics

Creates a customer in Baremetrics.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/:source_id/customers`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Create Customer](https://developers.baremetrics.com/reference/create-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source_id` | path | `string` | yes | Please see [Sources](ref:sources) |
| `name` | body | `string` | no | — |
| `notes` | body | `string` | no | Your own notes for this customer. These will be displayed in the profile |
| `email` | body | `string` | no | An email address for this customer. This is used to lookup extra profile information |
| `oid` | body | `string` | yes | Your unique ID for the customer |
| `created` | body | `string` | no | A unix timestamp of when this customer was created. Defaults to now. |
