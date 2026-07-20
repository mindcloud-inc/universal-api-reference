# Search User with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `organizations/:organizationId/users/search`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Search User](https://www.questionpro.com/api/search-user.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | The QuestionPro organization ID. |
| `emailAddress` | query | `string` | yes | The email address to search for. |
