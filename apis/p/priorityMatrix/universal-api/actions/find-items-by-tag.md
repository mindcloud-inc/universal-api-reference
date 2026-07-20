# Priority Matrix: Find Items By Tag

Finds Priority Matrix items by tag.

```
GET https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-items-by-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Priority Matrix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-items-by-tag?connectionId=$CONNECTION_ID&limit=25&offset=0&tagName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tagName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/priorityMatrix/latest/actions/find-items-by-tag?${params}`, {
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
| `tagName` | string | yes | Tag name to match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completionPercentage": 1,
      "creationDate": 1,
      "descriptionText": "string",
      "id": 1,
      "name": "Ava Chen",
      "owner": "string",
      "quadrant": 1,
      "resource_uri": "string",
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
| `descriptionText` | string |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | string |  |
| `quadrant` | number |  |
| `resource_uri` | string |  |
| `state` | number |  |

## Native endpoint

Through the native Priority Matrix API, this operation is `GET /api/v1/item/` (base URL `https://sync.appfluence.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-items-by-tag.md) for the provider-specific parameters and requirements.

