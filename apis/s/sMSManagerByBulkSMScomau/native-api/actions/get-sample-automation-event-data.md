# Get Sample Automation Event Data with SMS Manager by BulkSMS.com.au

## Endpoint

- **Method:** `GET`
- **Path:** `/automations/samples/:event_type`
- **Base URL:** `https://smsmanager.com.au/v2/api`
- **Official documentation:** [Get Sample Automation Event Data](https://smsmanager.com.au/v2/api_docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type` | path | `string` | yes | Automation event type to fetch sample data for. Accepted values: `dlr`, `mms_mo`, `sms_mo`. |
