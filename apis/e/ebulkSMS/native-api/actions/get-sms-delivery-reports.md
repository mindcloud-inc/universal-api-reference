# Get SMS Delivery Reports with EbulkSMS

Retrieves SMS delivery reports from EbulkSMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/getdlr.json`
- **Base URL:** `https://api.ebulksms.com`
- **Official documentation:** [Get SMS Delivery Reports](https://www.ebulksms.com/files/uploads/docs/ebulksms-api.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uniqueid` | query | `string` | no | Optional message ID to fetch delivery status for a specific SMS. |
