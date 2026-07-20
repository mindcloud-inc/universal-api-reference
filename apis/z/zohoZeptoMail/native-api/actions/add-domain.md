# Add Domain with Zoho ZeptoMail

Adds a new domain in Zoho ZeptoMail.

## Endpoint

- **Method:** `POST`
- **Path:** `domains`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Add Domain](https://www.zoho.com/zeptomail/help/api/add-domain.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_name` | body | `string` | yes | Domain to add to ZeptoMail. |
| `sub_domain_prefix` | body | `string` | yes | Subdomain prefix used for bounce tracking. |
| `mailagent_keys[0]` | body | `string` | yes | Agent alias to associate with the domain. |
