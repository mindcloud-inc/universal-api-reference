# Create lien filings in batch with Middesk

Creates lien filings in batch in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/businesses/:business_id/liens/batch`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create lien filings in batch](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose lien filings you want to create. |
| `liens[]` | body | `array` | yes | Lien filings to create in batch. |
