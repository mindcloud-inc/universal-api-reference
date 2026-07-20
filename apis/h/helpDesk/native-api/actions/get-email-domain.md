# Get Email Domain with HelpDesk

Retrieves an email domain from HelpDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/emailDomains/:domainID`
- **Base URL:** `https://api.helpdesk.com`
- **Official documentation:** [Get Email Domain](https://api.helpdesk.com/docs#tag/Email-domains/operation/emailDomainRead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainID` | path | `string` | yes | The HelpDesk email domain ID. |
