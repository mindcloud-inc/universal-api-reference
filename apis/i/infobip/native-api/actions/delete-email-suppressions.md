# Delete Email Suppressions with Infobip

## Endpoint

- **Method:** `DELETE`
- **Path:** `/email/1/suppressions`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Delete Email Suppressions](https://www.infobip.com/docs/api/channels/email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `suppressions` | body | `list<object>` | yes | Email addresses to delete from the suppression list. Number of destinations cannot exceed 10,000. |
| `suppressions.domainName` | body | `string` | no | Domain name from which suppressions will be deleted. |
| `suppressions.emailAddress` | body | `list<string>` | no | Email addresses that need to be deleted. |
| `suppressions.type` | body | `string` | no | Type of suppression. |
