# Get Partner Balance with Trak Qr Automation

Retrieves partner balance from Trak Qr Automation.

## Endpoint

- **Method:** `GET`
- **Path:** `/events-partners/balance`
- **Base URL:** `https://backend.trak.codes/api/v0`
- **Official documentation:** [Get Partner Balance](https://docs.google.com/document/u/2/d/e/2PACX-1vSFebcwRE1ntGhoYLQB90Ujf5BfUFocWmZWTfw1FGW3LawP3Q7ZDDOGwHEwsVQnwXJO2tdj1d8NQqit/pub?urp=gmail_link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | no | Optional attendee creation start date, inclusive, in ISO 8601 format. |
| `endDate` | query | `date` | no | Optional attendee creation end date, exclusive, in ISO 8601 format. |
