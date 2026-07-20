# List Domains with GoDaddy CRM

Retrieves domains from your GoDaddy account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/domains`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [List Domains](https://developer.godaddy.com/doc/endpoint/domains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statuses[]` | query | `array<string>` | no | Only include results with status values in the specified set. |
| `statusGroups[]` | query | `array<string>` | no | Only include results with status values in the specified groups. |
| `includes[]` | query | `array<string>` | no | Optional details to include in the response. |
| `modifiedDate` | query | `date` | no | Only include results modified since the specified date. |
