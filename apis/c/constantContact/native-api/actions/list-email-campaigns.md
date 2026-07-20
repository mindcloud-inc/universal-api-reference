# List Email Campaigns with Constant Contact

Retrieves email campaigns from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/emails`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [List Email Campaigns](https://developer.constantcontact.com/api_guide/email_campaigns_collection.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before_date` | query | `date` | no | Return campaigns updated before this ISO-8601 datetime. |
| `after_date` | query | `date` | no | Return campaigns updated after this ISO-8601 datetime. |
