# Score Activities with Scoreboard Buzz

Creates scored activities in Scoreboard Buzz in one request.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities`
- **Base URL:** `https://api.scoreboardbuzz.com/api/v1`
- **Official documentation:** [Score Activities](https://docs.scoreboardbuzz.com/#/Activities/createActivities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input[]` | body | `array<object>` | yes | Array of activities to score in one request. |
| `input[].user_id` | body | `number` | yes | ID of the user to score the activity for. |
| `input[].trackable_id` | body | `number` | yes | ID of the trackable to score. |
| `input[].product_name` | body | `string` | no | Optional product name for reference only. |
| `input[].quantity` | body | `number` | no | Number of units to score. Defaults to 1. |
| `input[].value` | body | `number` | no | Value amount to score. Defaults to 0. |
| `input[].memo` | body | `string` | no | Optional memo text for the activity. Maximum length: 500. |
