# Submit Whatsapp Template for review with Routee

Submits a WhatsApp template for review in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:whatsappAccountId/templates`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Submit Whatsapp Template for review](https://docs.routee.net/reference/submit-whatsapp-text-template-for-review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappAccountId` | path | `string` | yes | WhatsApp account id |
| `templateName` | body | `string` | no | The name of the Template. Max 512 ASCII char set |
| `templateCategory` | body | `string` | no | Category of the template. Fixed set as per documentation. |
| `localizations` | body | `string` | no | Localizations of the template |
| `language` | body | `string` | no | Supported language codes can be found at https://developers.facebook.com/docs/whatsapp/business-management-api/message-templates |
| `components` | body | `string` | no | Components the template is defined of |
| `componentType` | body | `string` | no | Determines the type of the component. Can be Header, Footer, Body, Buttons. |
| `text` | body | `string` | no | Template text |
| `format` | body | `string` | no | Which kind of header can be any of TEXT / IMAGE / DOCUMENT / VIDEO |
| `buttons[]` | body | `array<object>` | no | There can be up to 3 Quick reply buttons and Call to action buttons can be at most one of each button type for a maximum of 2 buttons. |
