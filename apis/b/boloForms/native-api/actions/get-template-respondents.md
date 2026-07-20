# Get Template Respondents with BoloForms

Retrieves respondents for a BoloForms template.

## Endpoint

- **Method:** `GET`
- **Path:** `/get-template-respondent`
- **Base URL:** `https://sapi.boloforms.com/signature`
- **Official documentation:** [Get Template Respondents](https://bolosign-developer-docs.readme.io/reference/get_get-template-respondent-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | query | `string` | yes | Template ID to retrieve respondents for |
| `respondentDocumentId` | query | `string` | no | Specific respondent ID to retrieve |
| `page` | query | `number` | no | Page number for pagination |
| `limit` | query | `number` | no | Number of respondents per page |
