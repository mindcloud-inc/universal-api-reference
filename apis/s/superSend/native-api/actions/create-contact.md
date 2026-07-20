# Create Contact with SuperSend

Creates a new contact in SuperSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Create Contact](https://docs.supersend.io/docs/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | — |
| `linkedin_url` | body | `string` | no | — |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `website` | body | `string` | no | — |
| `twitter` | body | `string` | no | — |
| `custom` | body | `object` | no | — |
| `TeamId` | body | `string` | yes | — |
| `CampaignId` | body | `string` | yes | — |
| `validate_emails` | body | `boolean` | no | When true, runs email verification on the contact (consumes credits). Default is false to avoid surprise billing. Only applies when creating a new contact with an email. |
