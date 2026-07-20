# Enrol Prospect in Lesson with Teach 'n Go

Enrols a prospect in a Teach 'n Go lesson.

## Endpoint

- **Method:** `POST`
- **Path:** `/globalApis/enrollProspect`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [Enrol Prospect in Lesson](https://intercom.help/teach-n-go/en/articles/5750592-prospect-registration-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lesson_id` | body | `string` | yes | The Teach 'n Go lesson ID to enrol the prospect into. |
| `prospect_id` | body | `string` | yes | The prospect ID to enrol. |
