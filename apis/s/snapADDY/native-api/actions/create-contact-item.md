# Create Contact Item with snapADDY

## Endpoint

- **Method:** `POST`
- **Path:** `/grabber/v1/contactitem`
- **Base URL:** `https://api.snapaddy.com`
- **Official documentation:** [Create Contact Item](https://developers.snapaddy.com/dataquality-rest-api/reference/create-contact-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments[]` | body | `array<string>` | yes | Attachment identifiers |
| `bcChecked` | body | `boolean` | yes | Whether the business card was checked |
| `bcImage` | body | `string` | yes | Business card image URL or content reference |
| `bcImageBackside` | body | `string` | yes | Business card backside image URL or content reference |
| `bcImageBacksideLocal` | body | `string` | yes | Local backside business card image reference |
| `bcImageLocal` | body | `string` | yes | Local business card image reference |
| `city` | body | `string` | yes | City |
| `companySize` | body | `string` | yes | Company size bucket |
| `contactListId` | body | `string` | yes | Contact list identifier |
| `country` | body | `string` | yes | Country code |
| `customFields` | body | `object` | yes | Custom field map |
| `drawing` | body | `string` | yes | Drawing data |
| `email` | body | `string` | yes | Email address |
| `facebook` | body | `string` | yes | Facebook profile URL |
| `fax` | body | `string` | yes | Fax number |
| `firstName` | body | `string` | yes | Contact first name |
| `gender` | body | `number` | yes | -1 neutral, 0 male, 1 female |
| `image` | body | `string` | yes | Profile image |
| `industry` | body | `string` | yes | Industry code |
| `lastName` | body | `string` | yes | Contact last name |
| `linkedin` | body | `string` | yes | LinkedIn profile URL |
| `mobile` | body | `string` | yes | Mobile number |
| `note` | body | `string` | yes | Contact note |
| `organization` | body | `string` | yes | Organization name |
| `phone` | body | `string` | yes | Phone number |
| `poBox` | body | `string` | yes | PO box |
| `position` | body | `string` | yes | Job position |
| `revenue` | body | `string` | yes | Revenue |
| `state` | body | `string` | yes | State or region |
| `street` | body | `string` | yes | Street address |
| `title` | body | `string` | yes | Honorific or salutation |
| `twitter` | body | `string` | yes | Twitter profile URL |
| `vat` | body | `string` | yes | VAT number |
| `website` | body | `string` | yes | Website URL |
| `xing` | body | `string` | yes | Xing profile URL |
| `zip` | body | `string` | yes | ZIP or postal code |
