# Create Or Update Lead with PeakIDX

Creates or updates a lead in PeakIDX.

## Endpoint

- **Method:** `POST`
- **Path:** `https://account.peakidxsites.com/lead-api/create-lead`
- **Base URL:** `https://account.peakidxsites.com`
- **Official documentation:** [Create Or Update Lead](https://docs.peakidx.com/api/lead-management-api#create-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | no | Unique identifier for the lead. |
| `lead_type` | body | `string` | no | Lead category such as Inquiry, Property Inquiry, CMA Inquiry, or Mortgage Quote. |
| `lead_first_name` | body | `string` | no | Lead given name. |
| `lead_last_name` | body | `string` | no | Lead family name. |
| `lead_email` | body | `string` | no | Primary lead email address. |
| `lead_phone` | body | `string` | no | Primary lead phone number. |
| `lead_comments` | body | `string` | no | Additional notes or context for the lead. |
| `lead_listing_id` | body | `string` | no | Associated listing identifier such as an MLS number. |
| `lead_phone2` | body | `string` | no | Secondary lead phone number. |
| `lead_created_datetime` | body | `string` | no | Lead creation timestamp in PeakIDX format such as 2024-03-22 12:00:00. |
| `lead_custom_fields` | body | `string` | no | Multi-line custom field text formatted as Label: Value pairs. |
