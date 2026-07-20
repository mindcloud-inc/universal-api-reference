# Create Customer with Metronome

Creates a new customer in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Create Customer](https://docs.metronome.com/api-reference/customers/create-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The customer name. |
| `ingest_aliases[]` | body | `array<string>` | no | Aliases that can identify the customer in usage events. Send multiple values as a array. |
| `external_id` | body | `string` | no | Deprecated alias that can identify the customer in usage events. |
