# Create Business with GatherUp

Creates a new business in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/create`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Create Business](https://app.gatherup.com/api/doc/business/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessName` | body | `string` | yes | Business name. |
| `businessOwnerAccount` | body | `number` | no | Set to 1 if you want to create business manager (aka User). |
| `businessOwnerEmail` | body | `string` | no | User email. |
| `businessOwnerFirstName` | body | `string` | no | User first name. |
| `businessOwnerLastName` | body | `string` | no | User last name. |
| `businessOwnerSendPasswordEmail` | body | `number` | no | Send email with password |
| `businessType` | body | `string` | yes | Google business type. |
| `city` | body | `string` | yes | Business city. |
| `country` | body | `string` | yes | Business country code or full name. |
| `customField` | body | `string` | no | Custom ID (whitelabeled accounts only). |
| `emailImage` | body | `string` | no | Email Picture. |
| `emailLogo` | body | `string` | no | Company Logo. |
| `feedbackBanner` | body | `string` | no | Feedback Page Banner. |
| `organisationType` | body | `string` | no | Organisation type: company, corporation, non profit, school, office, practice, agency, church,restaurant, event, firm, store, dealership |
| `phone` | body | `string` | yes | Mobile phone number. |
| `state` | body | `string` | yes | Business state code or full name. |
| `streetAddress` | body | `string` | yes | Business street address. |
| `websiteUrl` | body | `string` | no | Business website url. |
| `zip` | body | `string` | yes | Business zip code. |
| `language` | body | `string` | no | Business language |
