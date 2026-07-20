# Get Email Suppressions with Infobip

## Endpoint

- **Method:** `GET`
- **Path:** `/email/1/suppressions`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Get Email Suppressions](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainName` | query | `string` | yes | Name of the requested domain. |
| `type` | query | `string` | yes | Type of suppression. |
| `emailAddress` | query | `string` | no | Email address that is suppressed. |
| `recipientDomain` | query | `string` | no | Recipient domain that is suppressed. |
| `createdDateFrom` | query | `date` | no | Start date for searching suppressions. |
| `createdDateTo` | query | `date` | no | End date for searching suppressions. |
| `page` | query | `number` | no | Requested page number. |
| `size` | query | `number` | no | Requested page size. |
