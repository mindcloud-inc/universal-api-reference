# Find Contact with NextLead

Finds a contact in NextLead by email or LinkedIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/contact/find-contact`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Find Contact](https://dashboard.nextlead.app/en/api-documentation#receive-contact-find)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Contact email address to find. |
| `linkedin_url` | body | `string` | no | LinkedIn URL used when email is not provided. |
