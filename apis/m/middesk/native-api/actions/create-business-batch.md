# Create a business batch with Middesk

Creates a business batch in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/business_batches`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a business batch](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `csv` | body | `string` | yes | CSV content for the batch upload. |
| `filename` | body | `string` | yes | Filename associated with the uploaded CSV. |
| `name` | body | `string` | yes | Name for the business batch. |
