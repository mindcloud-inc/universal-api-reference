# Search Company Emails with Minelead

Finds company emails in Minelead by domain.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [Search Company Emails](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Company domain to search for emails. |
| `name` | query | `string` | no | Company name when searching without a domain. |
| `max-emails` | query | `number` | no | Maximum number of emails to display. |
| `generic` | query | `boolean` | no | Only return generic emails. |
| `light-mode` | query | `boolean` | no | Only display already found emails. |
