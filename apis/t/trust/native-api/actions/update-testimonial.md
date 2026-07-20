# Update Testimonial with Trust

Updates an existing testimonial in Trust.

## Endpoint

- **Method:** `PUT`
- **Path:** `/testimonial/:id`
- **Base URL:** `https://api.usetrust.app/v1`
- **Official documentation:** [Update Testimonial](https://api-docs.usetrust.io/api-reference-swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company` | body | `string` | no | Company of the testimonial giver. |
| `consentDateTime` | body | `date` | no | Date and time when consent was given. |
| `email` | body | `string` | no | Email address of the testimonial giver. |
| `externalVideoHtml` | body | `string` | no | Embeddable external video HTML. |
| `firstname` | body | `string` | no | First name of the testimonial giver. |
| `gaveConsent` | body | `boolean` | no | Whether the giver consented to publication. |
| `id` | path | `string` | yes | The testimonial ID. |
| `imageUrl` | body | `string` | no | Image URL for the testimonial giver. |
| `lastname` | body | `string` | no | Last name of the testimonial giver. |
| `published` | body | `boolean` | no | Whether the testimonial is published. |
| `socialMediaProfiles` | body | `string` | no | List of social media profile URLs. |
| `stars` | body | `number` | no | Star rating for the testimonial. |
| `subtitle` | body | `string` | no | Subtitle of the testimonial. |
| `testimonialText` | body | `string` | no | Text content of the testimonial. |
| `title` | body | `string` | no | Title of the testimonial. |
| `videoToken` | body | `string` | no | Token of an uploaded video. |
| `videoUrl` | body | `string` | no | URL of an uploaded video. |
| `workspaceId` | body | `string` | yes | The Trust workspace ID. |
