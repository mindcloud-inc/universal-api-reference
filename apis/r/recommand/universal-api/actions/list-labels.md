# Recommand: List Labels

Retrieves label records from the Recommand API.

```
GET https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-labels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recommand/latest/actions/list-labels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "labels": [
        {
          "colorHex": "string",
          "createdAt": "string",
          "externalId": "string",
          "id": "string",
          "name": "Ava Chen",
          "teamId": "string",
          "updatedAt": "string"
        }
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `labels` | array<object> |  |
| `labels[].colorHex` | string |  |
| `labels[].createdAt` | string |  |
| `labels[].externalId` | string |  |
| `labels[].id` | string |  |
| `labels[].name` | string |  |
| `labels[].teamId` | string |  |
| `labels[].updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `GET /api/v1/labels` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

