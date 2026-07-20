# Set Customer Ingest Aliases with Metronome

Creates or updates customer ingest aliases in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers/:customer_id/setIngestAliases`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Set Customer Ingest Aliases](https://docs.metronome.com/api-reference/customers/create-or-update-customer-ingest-aliases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The customer ID. |
| `ingest_aliases[]` | body | `array<string>` | yes | Customer ingest aliases. |
