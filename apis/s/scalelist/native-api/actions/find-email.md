# Find Email with Scalelist

Finds a contact email in Scalelist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ext/finder/email`
- **Base URL:** `https://app.scalelist.com`
- **Official documentation:** [Find Email](https://app.scalelist.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `full_name` | query | `string` | no | Full name of the person to look up. |
| `first_name` | query | `string` | no | First name of the person to look up. |
| `last_name` | query | `string` | no | Last name of the person to look up. |
| `company_name` | query | `string` | no | Company name to help the lookup. |
| `company_website` | query | `string` | no | Company website to help the lookup. |
