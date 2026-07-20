# Youform: List Form Submissions

Lists submissions for a form in Youform.

```
GET https://connect.mindcloud.co/v1/universal/youform/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Youform `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youform/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youform/latest/actions/list-form-submissions?${params}`, {
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
| `formSlug` | string | yes | Slug of the form whose submissions you want to list. |
| `isComplete` | boolean | no | Optional filter for completed vs partial submissions. Omit unless you explicitly need it. |
| `sortBy` | string | no | Field to sort submissions by, for example `created_at`. |
| `sortByOrder` | string | no | Sort direction for `sort_by`, for example `asc` or `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "formId": 1,
      "id": 1,
      "isComplete": 1,
      "uid": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `data` | object |  |
| `formId` | number |  |
| `id` | number |  |
| `isComplete` | number |  |
| `uid` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Youform API, this operation is `GET /forms/:formSlug/submissions` (base URL `https://app.youform.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

