# Priority Matrix: List Project Item Summaries

Retrieves item summaries from a Priority Matrix project.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-project-item-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-project-item-summaries?connectionId=$CONNECTION_ID&limit=25&offset=0&idd=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "idd": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/list-project-item-summaries?${params}`, {
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
| `idd` | number | yes | Project IDD. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completionPercentage": 1,
      "creationDate": 1,
      "id": 1,
      "name": "Ava Chen",
      "owner": "string",
      "quadrant": 1,
      "state": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completionPercentage` | number |  |
| `creationDate` | number |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | string |  |
| `quadrant` | number |  |
| `state` | number |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `GET /api/v1/project/:idd/item_summaries/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-item-summaries.md) for the provider-specific parameters and requirements.

