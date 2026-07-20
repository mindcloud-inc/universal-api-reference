# <img src="https://images.mindcloud.co/apps/icons/passslot-icon_1775158668661.png" alt="Passslot logo" width="28" height="28"> Passslot: Universal API

Create, update, distribute, and manage Apple Wallet and Google Wallet passes through the Passslot REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/passslot/latest
- **Category:** Marketing
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.passslot.com
- **Vendor API docs:** https://www.passslot.com/developer/api/start

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passslot/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Actions](actions/get-template-actions.md) | GET |  |
| [Update Template Actions](actions/update-template-actions.md) | PUT |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Pass](actions/delete-pass.md) | DELETE |  |
| [Get Pass Description](actions/get-pass-description.md) | GET |  |
| [Get Pass Link](actions/get-pass-link.md) | GET |  |
| [Get Pass Values](actions/get-pass-values.md) | GET |  |
| [List Passes](actions/list-passes.md) | GET |  |
| [List Passes By Pass Type](actions/list-passes-by-pass-type.md) | GET |  |
| [Push Pass](actions/push-pass.md) | PUT |  |
| [Send Pass by Email](actions/send-pass-by-email.md) | PUT |  |
| [Update Pass Value](actions/update-pass-value.md) | PUT |  |
| [Update Pass Values](actions/update-pass-values.md) | PUT |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Create Scanner](actions/create-scanner.md) | POST |  |
| [Delete Scanner](actions/delete-scanner.md) | DELETE |  |
| [Get Scanner](actions/get-scanner.md) | GET |  |
| [List Scanners](actions/list-scanners.md) | GET |  |
| [Update Scanner](actions/update-scanner.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Delete Template Footer Image](actions/delete-template-footer-image.md) | DELETE |  |
| [Update Template Footer Image](actions/update-template-footer-image.md) | PUT |  |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Pass Type](actions/get-pass-type.md) | GET |  |
| [List Pass Types](actions/list-pass-types.md) | GET |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Payment Settings](actions/get-template-payment-settings.md) | GET |  |
| [Update Template Payment Settings](actions/update-template-payment-settings.md) | PUT |  |

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Get Template Distribution Restrictions](actions/get-template-distribution-restrictions.md) | GET |  |
| [Update Template Distribution Restrictions](actions/update-template-distribution-restrictions.md) | PUT |  |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Delete Pass Price](actions/delete-pass-price.md) | DELETE |  |
| [Get Pass Price](actions/get-pass-price.md) | GET |  |
| [Update Pass Price](actions/update-pass-price.md) | PUT |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Pass Status](actions/get-pass-status.md) | GET |  |
| [Update Pass Status](actions/update-pass-status.md) | PUT |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Delete Template](actions/delete-template.md) | DELETE |  |
| [Get Template](actions/get-template.md) | GET |  |
| [Get Template Branding Settings](actions/get-template-branding-settings.md) | GET |  |
| [Get Template Link](actions/get-template-link.md) | GET |  |
| [List Templates](actions/list-templates.md) | GET |  |
| [Update Template](actions/update-template.md) | PUT |  |
| [Update Template Branding Settings](actions/update-template-branding-settings.md) | PUT |  |

