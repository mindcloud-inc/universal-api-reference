# Swell: List Promotions



```
GET https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-promotions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-promotions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swell/latest/actions/list-promotions?${params}`, {
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
      "active": true,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEnd": "2026-05-07T12:00:00.000Z",
      "dateStart": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discounts": [
        {
          "type": "string",
          "valueFixed": 1,
          "valueType": "string"
        }
      ],
      "id": "string",
      "name": "Ava Chen",
      "useCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `dateEnd` | date |  |
| `dateStart` | date |  |
| `description` | string |  |
| `discounts[].type` | string |  |
| `discounts[].valueFixed` | number |  |
| `discounts[].valueType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `useCount` | number |  |

## Native endpoint

Through the native Swell API, this operation is `GET /promotions` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-promotions.md) for the provider-specific parameters and requirements.

