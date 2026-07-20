# Email BI Report with Billetto

Sends a business intelligence report from Billetto by email.

## Endpoint

- **Method:** `POST`
- **Path:** `organiser/events/{eventid}/bi_report/by_email/`
- **Base URL:** `https://billetto.dk/api/v3`
- **Official documentation:** [Email BI Report](https://api.billetto.com/reference/order-a-business-intelligence-report-sent-to-a-specified-endpoint-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventid` | path | `string` | yes | Billetto event ID. |
