# Update Domain with Zoho ZeptoMail

Updates an existing domain in Zoho ZeptoMail.

## Endpoint

- **Method:** `PUT`
- **Path:** `domains/:domainKey`
- **Base URL:** `https://api.zeptomail.com/v1.1`
- **Official documentation:** [Update Domain](https://www.zoho.com/zeptomail/help/api/edit-domain.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domainKey` | path | `string` | yes | Domain key from ZeptoMail. |
| `new_domain` | body | `string` | no | Replacement domain name. |
| `new_sub_domain_prefix` | body | `string` | no | Replacement bounce subdomain prefix. |
| `associate_mailagents[0]` | body | `string` | no | Agent alias to associate with the domain. |
| `unassociate_mailagents[0]` | body | `string` | no | Agent alias to disassociate from the domain. |
