# Add Question to Service with CodeREADr

Adds a question to a scanning service in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Add Question to Service](https://secure.codereadr.com/apidocs/Services.md#add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service_id` | body | `string` | yes | Service or services to attach the question to. |
| `question_id` | body | `string` | yes | Question or questions to attach to the service. |
| `condition` | body | `string` | no | When the question should appear, such as pre_submit or valid_scan. |
| `required` | body | `string` | no | Question IDs that should be mandatory to answer when added. |
