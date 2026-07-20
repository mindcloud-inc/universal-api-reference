# Passslot: Native API Reference

A consolidated summary of Passslot's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://www.passslot.com/developer/api/start
- **API base URL:** `https://api.passslot.com/v1`

## Authentication

### API Key

Authenticate Passslot API requests with your Passslot App Key sent in the Authorization header.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.passslot.com/developer/api/start)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Scanner](actions/create-scanner.md) | `POST scanners` | [docs](https://www.passslot.com/developer/api/resources/createScanner) |
| [Create Template](actions/create-template.md) | `POST templates` | [docs](https://www.passslot.com/developer/api/resources/createTemplate) |
| [Delete Pass](actions/delete-pass.md) | `DELETE passes/:passTypeIdentifier/:serialNumber` | [docs](https://www.passslot.com/developer/api/resources/deletePass) |
| [Delete Pass Price](actions/delete-pass-price.md) | `DELETE passes/:passTypeIdentifier/:serialNumber/price` | [docs](https://www.passslot.com/developer/api/resources/deletePassPrice) |
| [Delete Scanner](actions/delete-scanner.md) | `DELETE scanners/:id` | [docs](https://www.passslot.com/developer/api/resources/deleteScanner) |
| [Delete Template](actions/delete-template.md) | `DELETE templates/:id` | [docs](https://www.passslot.com/developer/api/resources/deleteTemplate) |
| [Delete Template Footer Image](actions/delete-template-footer-image.md) | `DELETE templates/:id/branding/footer/image` | [docs](https://www.passslot.com/developer/api/resources/deleteTemplateBrandingFooterImage) |
| [Get Pass Description](actions/get-pass-description.md) | `GET passes/:passTypeIdentifier/:serialNumber/passjson` | [docs](https://www.passslot.com/developer/api/resources/showPassJSON) |
| [Get Pass Link](actions/get-pass-link.md) | `GET passes/:passTypeIdentifier/:serialNumber/url` | [docs](https://www.passslot.com/developer/api/resources/showPassURL) |
| [Get Pass Price](actions/get-pass-price.md) | `GET passes/:passTypeIdentifier/:serialNumber/price` | [docs](https://www.passslot.com/developer/api/resources/showPassPrice) |
| [Get Pass Status](actions/get-pass-status.md) | `GET passes/:passTypeIdentifier/:serialNumber/status` | [docs](https://www.passslot.com/developer/api/resources/showPassStatus) |
| [Get Pass Type](actions/get-pass-type.md) | `GET passtypes/:id` | [docs](https://www.passslot.com/developer/api/resources/showPassType) |
| [Get Pass Values](actions/get-pass-values.md) | `GET passes/:passTypeIdentifier/:serialNumber/values` | [docs](https://www.passslot.com/developer/api/resources/showPassValues) |
| [Get Scanner](actions/get-scanner.md) | `GET scanners/:id` | [docs](https://www.passslot.com/developer/api/resources/showScanner) |
| [Get Template](actions/get-template.md) | `GET templates/:id` | [docs](https://www.passslot.com/developer/api/resources/showTemplate) |
| [Get Template Actions](actions/get-template-actions.md) | `GET templates/:id/actions` | [docs](https://www.passslot.com/developer/api/resources/showTemplateActions) |
| [Get Template Branding Settings](actions/get-template-branding-settings.md) | `GET templates/:id/branding` | [docs](https://www.passslot.com/developer/api/resources/showTemplateBranding) |
| [Get Template Distribution Restrictions](actions/get-template-distribution-restrictions.md) | `GET templates/:id/restrictions` | [docs](https://www.passslot.com/developer/api/resources/showTemplateRestrictions) |
| [Get Template Link](actions/get-template-link.md) | `GET templates/:id/url` | [docs](https://www.passslot.com/developer/api/resources/showTemplateURL) |
| [Get Template Payment Settings](actions/get-template-payment-settings.md) | `GET templates/:id/payment` | [docs](https://www.passslot.com/developer/api/resources/showTemplatePayment) |
| [List Pass Types](actions/list-pass-types.md) | `GET passtypes` | [docs](https://www.passslot.com/developer/api/resources/listPassTypes) |
| [List Passes](actions/list-passes.md) | `GET passes` | [docs](https://www.passslot.com/developer/api/resources/listPasses) |
| [List Passes By Pass Type](actions/list-passes-by-pass-type.md) | `GET passes/:passTypeIdentifier` | [docs](https://www.passslot.com/developer/api/resources/listPassesByPassType) |
| [List Scanners](actions/list-scanners.md) | `GET scanners` | [docs](https://www.passslot.com/developer/api/resources/listScanners) |
| [List Templates](actions/list-templates.md) | `GET templates` | [docs](https://www.passslot.com/developer/api/resources/listTemplates) |
| [Push Pass](actions/push-pass.md) | `POST passes/:passTypeIdentifier/:serialNumber/push` | [docs](https://www.passslot.com/developer/api/resources/pushPass) |
| [Send Pass by Email](actions/send-pass-by-email.md) | `POST passes/:passTypeIdentifier/:serialNumber/email` | [docs](https://www.passslot.com/developer/api/resources/sendPassEmail) |
| [Update Pass Price](actions/update-pass-price.md) | `PUT passes/:passTypeIdentifier/:serialNumber/price` | [docs](https://www.passslot.com/developer/api/resources/updatePassPrice) |
| [Update Pass Status](actions/update-pass-status.md) | `PUT passes/:passTypeIdentifier/:serialNumber/status` | [docs](https://www.passslot.com/developer/api/resources/updatePassStatus) |
| [Update Pass Value](actions/update-pass-value.md) | `PUT passes/:passTypeIdentifier/:serialNumber/value/:placeholderName` | [docs](https://www.passslot.com/developer/api/resources/updatePassValue) |
| [Update Pass Values](actions/update-pass-values.md) | `PUT passes/:passTypeIdentifier/:serialNumber/values` | [docs](https://www.passslot.com/developer/api/resources/updatePassValues) |
| [Update Scanner](actions/update-scanner.md) | `PUT scanners/:id` | [docs](https://www.passslot.com/developer/api/resources/updateScanner) |
| [Update Template](actions/update-template.md) | `PUT templates/:id` | [docs](https://www.passslot.com/developer/api/resources/updateTemplate) |
| [Update Template Actions](actions/update-template-actions.md) | `PUT templates/:id/actions` | [docs](https://www.passslot.com/developer/api/resources/updateTemplateActions) |
| [Update Template Branding Settings](actions/update-template-branding-settings.md) | `PUT templates/:id/branding` | [docs](https://www.passslot.com/developer/api/resources/updateTemplateBranding) |
| [Update Template Distribution Restrictions](actions/update-template-distribution-restrictions.md) | `PUT templates/:id/restrictions` | [docs](https://www.passslot.com/developer/api/resources/updateTemplateRestrictions) |
| [Update Template Footer Image](actions/update-template-footer-image.md) | `PUT templates/:id/branding/footer/image` | [docs](https://www.passslot.com/developer/api/resources/updateTemplateBrandingFooterImage) |
| [Update Template Payment Settings](actions/update-template-payment-settings.md) | `PUT templates/:id/payment` | [docs](https://www.passslot.com/developer/api/resources/updateTemplatePayment) |
