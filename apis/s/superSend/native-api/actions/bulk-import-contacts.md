# Bulk Import Contacts with SuperSend

Creates multiple contacts in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/bulk`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Bulk Import Contacts](https://docs.supersend.io/docs/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes | — |
| `contacts[].email` | body | `string` | no | — |
| `contacts[].linkedin_url` | body | `string` | no | — |
| `contacts[].twitter` | body | `string` | no | — |
| `contacts[].first_name` | body | `string` | no | — |
| `contacts[].last_name` | body | `string` | no | — |
| `contacts[].company_name` | body | `string` | no | — |
| `contacts[].title` | body | `string` | no | — |
| `contacts[].phone` | body | `string` | no | — |
| `contacts[].city` | body | `string` | no | — |
| `contacts[].state` | body | `string` | no | — |
| `contacts[].country` | body | `string` | no | — |
| `contacts[].industry` | body | `string` | no | — |
| `contacts[].company_url` | body | `string` | no | — |
| `contacts[].note` | body | `string` | no | — |
| `contacts[].one_liner` | body | `string` | no | — |
| `contacts[].custom` | body | `object` | no | — |
| `TeamId` | body | `string` | yes | — |
| `CampaignId` | body | `string` | yes | — |
| `validate_emails` | body | `boolean` | no | When true, runs email verification on imported contacts (consumes credits). Default false to avoid surprise billing. |
