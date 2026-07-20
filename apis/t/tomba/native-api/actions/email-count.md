# Email Count with Tomba

Retrieves the email count for a company in Tomba.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-count`
- **Base URL:** `https://api.tomba.io/v1`
- **Official documentation:** [Email Count](https://docs.tomba.io/api/finder#email-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Domain to count email coverage for. |
