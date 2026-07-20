# Formstack: List Form Submissions

Retrieves submissions for a form from Formstack.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-form-submissions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formId` | list<number> | yes | The unique identifier of the form to retrieve submissions from. |
| `keyword` | string | no | Search term to filter submissions by content across all fields. |
| `order` | list<string> | no | Sort order for results (ASC or DESC). One of: `ASC`, `DESC`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minTime` | date | no | Return submissions created on or after this date/time. |
| `maxTime` | date | no | Return submissions created on or before this date/time. |
| `search[]` | array<object> | no | Array of search criteria to filter submissions by specific field values. |
| `search[].fieldId` | string | no | The ID of the field to search. |
| `search[].value` | string | no | The value to search for in the field. |
| `data` | list<string> | no | Include field data in the response (true/false). One of: `false`, `true`. |
| `expandData` | list<string> | no | Include expanded field data with parsed values (true/false). One of: `false`, `true`. |
| `prettyName` | list<string> | no | Include a human-readable name for each submission (true/false). One of: `false`, `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "formId": 1,
      "id": 1,
      "prettyName": "Ava Chen",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Submission field data when requested. |
| `formId` | number | The ID of the form this submission belongs to. |
| `id` | number | The ID of the submission. |
| `prettyName` | string | Human-readable submission name when requested. |
| `timestamp` | date | Timestamp of the submission. |

## Native endpoint

Through the native Formstack API, this operation is `GET /forms/:formId/submissions` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

