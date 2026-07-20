# Get Invoices with Datalyse

Retrieves invoices for the authenticated agent from Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/companyuserdata/invoicesget.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Get Invoices](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_end` | body | `string` | no | End timestamp for date range filter (optional) |
| `date_start` | body | `string` | no | Start timestamp for date range filter (optional) |
