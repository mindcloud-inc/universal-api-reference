# Generate Word Search Grid with Shadify

Retrieves a random word search grid from Shadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/wordsearch/generator`
- **Base URL:** `https://shadify.yurace.pro/api`
- **Official documentation:** [Generate Word Search Grid](https://shadify.yurace.pro/modules/wordsearch.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `width` | query | `number` | no | Optional grid width from 5 to 20. Total cells must not exceed 256. Default is 9. |
| `height` | query | `number` | no | Optional grid height from 5 to 20. Total cells must not exceed 256. Default is 9. |
