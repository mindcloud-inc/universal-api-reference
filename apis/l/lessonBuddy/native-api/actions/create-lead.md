# Create Lead with LessonBuddy

Creates a new lead in LessonBuddy.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/campaign/leads`
- **Base URL:** `https://api.lessonbuddy.com`
- **Official documentation:** [Create Lead](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | body | `number` | yes | LessonBuddy location ID for the lead. |
| `firstName` | body | `string` | yes | Lead first name. At least one of first name or last name is required by LessonBuddy. |
| `lastName` | body | `string` | yes | Lead last name. At least one of first name or last name is required by LessonBuddy. |
| `emailAddress` | body | `string` | yes | Lead email address. At least one contact method, email or cell phone, is required by LessonBuddy. |
| `cellPhone` | body | `string` | no | Lead cell phone. At least one contact method, email or cell phone, is required by LessonBuddy. |
| `marketingOptIn` | body | `boolean` | no | Whether the customer consented to marketing opt-in. |
| `tags[].tag` | body | `string` | no | Lead tag. LessonBuddy recommends complete-lead-form. |
