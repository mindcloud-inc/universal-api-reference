# Insert NPS Survey Response with SatisMeter

## Endpoint

- **Method:** `POST`
- **Path:** `/api/responses`
- **Base URL:** `https://app.satismeter.com`
- **Official documentation:** [Insert NPS Survey Response](https://support.satismeter.com/hc/en-us/articles/6980464243475-Insert-response-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `writeKey` | body | `string` | yes | SatisMeter survey write key for response insertion. |
| `userId` | body | `string` | yes | External user identifier for the disposable or real survey respondent. |
| `score` | body | `number` | yes | NPS score value for the rating question. |
| `comment` | body | `string` | no | Free-text answer for the comment question. |
| `name` | body | `string` | no | Optional respondent name sent into traits. |
| `email` | body | `string` | no | Optional respondent email sent into traits. |
| `forceSurvey` | body | `boolean` | no | When true, allows creating the response even if survey rules would normally suppress it. |
