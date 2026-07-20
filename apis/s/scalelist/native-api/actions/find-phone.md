# Find Phone with Scalelist

Finds a contact phone number in Scalelist.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ext/finder/phone`
- **Base URL:** `https://app.scalelist.com`
- **Official documentation:** [Find Phone](https://app.scalelist.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkedin_profile_url` | query | `string` | no | LinkedIn profile URL of the person. |
| `linkedin_id` | query | `string` | no | LinkedIn ID of the person. |
| `email` | query | `string` | no | Email address of the person. |
| `full_name` | query | `string` | no | Full name of the person to look up. |
| `first_name` | query | `string` | no | First name of the person to look up. |
| `last_name` | query | `string` | no | Last name of the person to look up. |
| `company_name` | query | `string` | no | Company name to help the lookup. |
| `company_website` | query | `string` | no | Company website to help the lookup. |
| `job_title` | query | `string` | no | Job title of the person. |
| `city` | query | `string` | no | City of the person. |
