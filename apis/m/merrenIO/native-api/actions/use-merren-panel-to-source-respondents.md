# Use Merren Panel To Source Respondents with MerrenIO

## Endpoint

- **Method:** `GET`
- **Path:** `/deploy/getOnGoingSurveys/:surveyId`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Use Merren Panel To Source Respondents](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey identifier to inspect panel sourcing state for. |
| `page` | query | `string` | yes | Results page number. |
| `size` | query | `string` | yes | Number of rows to fetch. |
