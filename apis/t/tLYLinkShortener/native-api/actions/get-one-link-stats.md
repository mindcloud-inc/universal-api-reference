# Get OneLink Stats with TLY Link Shortener

Retrieves stats for a OneLink in TLY Link Shortener.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/onelink/stats`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Get OneLink Stats](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | query | `string` | yes | The OneLink short URL to retrieve stats for. |
| `start_date` | query | `date` | no | Optional UTC start date for the stats window. |
| `end_date` | query | `date` | no | Optional UTC end date for the stats window. |
