# Fillout Forms: List Submissions

Retrieves submissions for a Fillout form.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-submissions?${params}`, {
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
| `formId` | string | yes | The form ID to list submissions for. |
| `status` | string | no | Filter submissions by completion status. |
| `search` | string | no | Free-text search across submissions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `afterDate` | date | no | Return submissions created after this date-time. |
| `beforeDate` | date | no | Return submissions created before this date-time. |
| `includeEditLink` | boolean | no | Include edit links in response items. |
| `includePreview` | boolean | no | Whether to include a preview of the submission content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageCount": 1,
      "responses": [
        {}
      ],
      "totalResponses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageCount` | number | Total number of pages for the current pagination window. |
| `responses` | array<object> | Submitted form responses. |
| `totalResponses` | number | Total number of submissions. |

## Native endpoint

Through the native Fillout Forms API, this operation is `GET /forms/:formId/submissions` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

