# Update Business with GatherUp

Updates an existing business in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/update`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Update Business](https://app.gatherup.com/api/doc/business/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `automatedEmailsPerDay` | body | `number` | no | Automatic emails per day. 0 = manual mode. |
| `businessId` | body | `number` | yes | Business id. |
| `businessName` | body | `string` | no | Business name. |
| `businessOwnerEmail` | body | `string` | no | User email. |
| `businessOwnerFirstName` | body | `string` | no | User first name. |
| `businessOwnerLastName` | body | `string` | no | User last name. |
| `businessType` | body | `string` | yes | Google business type. |
| `city` | body | `string` | no | Business city. |
| `country` | body | `string` | no | Business country code or full name. |
| `customField` | body | `string` | no | Custom ID (whitelabeled accounts only). |
| `emailImage` | body | `string` | no | Email Picture. |
| `emailLogo` | body | `string` | no | Company Logo. |
| `feedbackBanner` | body | `string` | no | Feedback Page Banner. |
| `organisationType` | body | `string` | no | Organisation type: company, corporation, non profit, school, office, practice, agency, church, restaurant, event, firm, store, dealership |
| `phone` | body | `string` | no | Mobile phone number. |
| `state` | body | `string` | no | Business state code or full name. |
| `streetAddress` | body | `string` | no | Business street address. |
| `websiteUrl` | body | `string` | no | Business website url. |
| `zip` | body | `string` | no | Business zip code. |
| `feedbackThreshold` | body | `number` | no | Defines the NPS score threshold for feedbacks received to be automatically approved to show on the testimonials widget. |
| `pageThreshold` | body | `number` | no | Defines the NPS score of what is considered positive or negative feedback. For example if set to 5 - any customer leaving an NPS score of 5 or above will be shown the positive feedback page. |
| `language` | body | `string` | no | Business language |
