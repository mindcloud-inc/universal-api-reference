# Score Domain Quality with Cloudmersive Data Validation

Scores domain quality with Cloudmersive Data Validation.

## Endpoint

- **Method:** `POST`
- **Path:** `/validate/domain/quality-score`
- **Base URL:** `https://api.cloudmersive.com`
- **Official documentation:** [Score Domain Quality](https://api.cloudmersive.com/docs/validate.asp)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain name to score. |
