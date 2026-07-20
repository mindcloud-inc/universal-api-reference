# Add Email Suppressions with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/email/1/suppressions`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Add Email Suppressions](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suppressions` | body | `list<object>` | yes | Email addresses to add to the suppression list. Number of destinations cannot exceed 10,000. |
| `suppressions.domainName` | body | `string` | no | Domain name from which suppressions will be added. |
| `suppressions.emailAddress` | body | `list<string>` | no | Email addresses to add to suppression list. |
| `suppressions.type` | body | `string` | no | Type of suppression. |
