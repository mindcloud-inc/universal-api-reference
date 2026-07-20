# Hey Reach: Get List

Retrieves a lead or company list from Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-list?connectionId=$CONNECTION_ID&listId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-list?${params}`, {
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
| `listId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignIds": [
        "string"
      ],
      "creationTime": "string",
      "id": "string",
      "listType": "string",
      "name": "Ava Chen",
      "totalItemsCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignIds` | array<string> |  |
| `creationTime` | string |  |
| `id` | string |  |
| `listType` | string |  |
| `name` | string |  |
| `totalItemsCount` | string |  |

## Native endpoint

Through the native Hey Reach API, this operation is `GET /api/public/list/GetById` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

