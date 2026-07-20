# Get UTM Code with LessonBuddy

Finds a UTM code in LessonBuddy by tracking parameters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/campaign/utm-codes`
- **Base URL:** `https://api.lessonbuddy.com`
- **Official documentation:** [Get UTM Code](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `utm_source` | query | `string` | yes | Specific traffic source, such as direct, google, facebook, or newsletter. |
| `utm_medium` | query | `string` | no | General traffic medium, such as social, email, or website. |
| `utm_campaign` | query | `string` | no | Campaign name, such as npo_promo or fall_sale. |
| `utm_term` | query | `string` | no | Optional paid-search term or keyword. |
| `utm_content` | query | `string` | no | Optional content identifier used to distinguish campaign variants. |
