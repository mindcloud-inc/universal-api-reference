# List New Leads with PeakIDX

Retrieves new leads from PeakIDX since the last sync.

## Endpoint

- **Method:** `GET`
- **Path:** `https://account.peakidxsites.com/lead-api/new-leads`
- **Base URL:** `https://account.peakidxsites.com`
- **Official documentation:** [List New Leads](https://docs.peakidx.com/api/lead-management-api#new-leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_type` | query | `string` | no | Optional comma-separated PeakIDX lead type names, such as Inquiry or Property Inquiry. |
