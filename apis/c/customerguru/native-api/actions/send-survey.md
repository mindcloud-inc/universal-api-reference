# Send Survey with Customer.guru

Creates a new survey send request in Customer.guru.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/survey`
- **Base URL:** `https://customer.guru`
- **Official documentation:** [Send Survey](https://customer.guru/api/documentation/v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `test` | body | `boolean` | no | When true, validate without sending emails. |
| `scheduled_for` | body | `string` | yes | Use now or an ISO8601 timestamp in the future. |
| `survey_id` | body | `number` | no | Optional specific survey ID. |
| `customers[]` | body | `array<object>` | yes | Array of customer objects with email and optional language and properties fields. |
