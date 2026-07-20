# Initiate Bulk Read Job with Zoho Recruit

Initiates a bulk read job in Zoho Recruit.

## Endpoint

- **Method:** `POST`
- **Path:** `https://recruit.zoho.com/recruit/bulk/v2/read`
- **Base URL:** `https://recruit.zoho.com/recruit/v2`
- **Official documentation:** [Initiate Bulk Read Job](https://www.zoho.com/recruit/developer-guide/apiv2/bulk-read/create-job.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `object` | yes | Bulk-read query object describing the module and export filters. |
| `callback` | body | `object` | no | Callback object that Zoho should notify when the bulk-read job finishes. |
| `file_type` | body | `string` | no | Export file type, such as ics for Events exports. Accepted values: `ics`. |
