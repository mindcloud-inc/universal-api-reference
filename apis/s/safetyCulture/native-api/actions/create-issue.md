# Create Issue with SafetyCulture

Creates a new issue in SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/incidents/submit`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Create Issue](https://developer.safetyculture.com/reference/incidentsservice_submitincident)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `string` | no | Optional. The unique identifier of the incident If not provided, UUID will be generated server side |
| `title` | body | `string` | yes | Required. Title of the incident Title is limited to only 255 characters max |
| `created_at` | body | `date` | no | Optional. Date and time this incident was created |
| `category_id` | body | `string` | yes | Required. ID of the incident's category If not set, this incident will be stored with the default category(None) |
| `answered_questions[]` | body | `array<string>` | no | Optional. An array of all, if any, custom questions that have been answered by the contributor @deprecated: Use `QuestionAnswer` instead. This was a field used for string custom questions. We've since moved to structured custom questions in the `QuestionAnswer` field. |
| `email` | body | `string` | no | Optional. The email address of the contributor |
| `media[]` | body | `array<object>` | no | Optional. Array of media items to be linked to the incident. |
| `site_id` | body | `string` | no | Optional. ID of the site to associate with the incident. If not provided, no site will be associated with the incident. |
| `name` | body | `string` | no | Optional. The name of the contributor |
| `contact` | body | `string` | no | Optional. The contact details of the contributor |
| `location` | body | `object` | no | The location that the incident occurred at |
| `access_token` | body | `string` | no | Optional. The access token used to authenticate the request. This field should be set when following the contributor flow. Otherwise, authenticate via normal means. |
| `description` | body | `string` | no | Optional. Description of the issue (maximum 500 characters). |
| `questions_and_answers[]` | body | `array<object>` | no | Optional. An array of all, if any, custom questions that have been answered for this issue. |
| `items[]` | body | `array<object>` | no | Optional. The category fields and questions that applied to this incident when it was created. |
| `occurred_at` | body | `date` | no | Optional. Date and time this incident occurred at |
| `asset_id` | body | `string` | no | Optional. The ID of the asset associated with this incident. |
