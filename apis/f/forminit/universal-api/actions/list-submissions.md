# Forminit: List Submissions

Retrieves submissions for a specific Forminit form.

```
GET https://connect.mindcloud.co/v1/universal/forminit/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Forminit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forminit/latest/actions/list-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forminit/latest/actions/list-submissions?${params}`, {
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
| `formId` | string | yes | Form identifier to read submissions from. |
| `query` | string | no | Search term used to filter matching submissions. |
| `files` | boolean | no | Include file details in the response when true. |
| `timezone` | string | no | IANA timezone used for formatted submission dates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "fields": [
        {
          "label": "string",
          "name": "Ava Chen",
          "sortOrder": 1,
          "type": "string"
        }
      ],
      "formId": "string",
      "pagination": {
        "count": 1,
        "currentPage": 1,
        "firstPage": 1,
        "lastPage": 1,
        "size": 1,
        "total": 1
      },
      "submissions": [
        {
          "blocks": {},
          "id": "string",
          "isSeen": true,
          "isStarred": true,
          "submissionDate": "2026-05-07T12:00:00.000Z",
          "submissionStatus": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string | Forminit API version reported by the endpoint. |
| `fields` | array<object> | Field definitions configured for the form. |
| `fields[].label` | string |  |
| `fields[].name` | string |  |
| `fields[].sortOrder` | number |  |
| `fields[].type` | string |  |
| `formId` | string | Form identifier returned by Forminit. |
| `pagination` | object | Pagination metadata for the current result set. |
| `pagination.count` | number |  |
| `pagination.currentPage` | number |  |
| `pagination.firstPage` | number |  |
| `pagination.lastPage` | number |  |
| `pagination.size` | number |  |
| `pagination.total` | number |  |
| `submissions` | array<object> | Matching submissions for the form. |
| `submissions[].blocks` | object |  |
| `submissions[].id` | string |  |
| `submissions[].isSeen` | boolean |  |
| `submissions[].isStarred` | boolean |  |
| `submissions[].submissionDate` | date |  |
| `submissions[].submissionStatus` | string |  |

## Native endpoint

Through the native Forminit API, this operation is `GET /v1/forms/:formId` (base URL `https://api.forminit.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

