# Common Ninja: List Submissions

Retrieves project submissions from Common Ninja.

```
GET https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Common Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/list-submissions?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/commonNinja/latest/actions/list-submissions?${params}`, {
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
| `projectId` | string | yes | The project ID. |
| `limit` | number | no | Maximum number of submissions to return. |
| `widgetId` | string | no | Filter submissions by widget ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docs": [
        {}
      ],
      "limit": 1,
      "offset": 1,
      "page": 1,
      "pages": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docs` | array<object> |  |
| `limit` | number |  |
| `offset` | number |  |
| `page` | number |  |
| `pages` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Common Ninja API, this operation is `GET /projects/:projectId/submissions` (base URL `https://api.commoninja.com/platform/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

