# Generate Capital Quiz with Shadify

Retrieves a capital quiz from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/countries/capital-quiz`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Capital Quiz](https://shadify.yurace.pro/modules/countries.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variants` | query | `number` | no | Optional number of answer variants from 2 to 6. Default is 4. |
| `amount` | query | `number` | no | Optional number of unique quizzes from 1 to 20. Default is 1. |
