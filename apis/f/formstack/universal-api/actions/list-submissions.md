# Formstack: List Submissions

Retrieves submissions across all forms from Formstack.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/list-submissions?${params}`, {
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
| `search` | string | yes | Search term to filter submissions by content. |
| `order` | list<string> | no | Sort order for results (ASC or DESC). One of: `ASC`, `DESC`. |

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

Through the native Formstack API, this operation is `GET /submissions` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

