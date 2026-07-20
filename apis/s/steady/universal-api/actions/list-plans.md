# Steady: List Plans

Retrieves membership plans for a Steady publication.

```
GET https://connect.mindcloud.co/v1/universal/steady/latest/actions/list-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Steady `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/steady/latest/actions/list-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/steady/latest/actions/list-plans?${params}`, {
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
      "data": [
        {
          "attributes": {
            "currency": "string",
            "giftable": true,
            "hidden": true,
            "name": "Ava Chen",
            "state": "string"
          },
          "id": "string",
          "type": "string"
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
| `data[].attributes.currency` | string |  |
| `data[].attributes.giftable` | boolean |  |
| `data[].attributes.hidden` | boolean |  |
| `data[].attributes.name` | string |  |
| `data[].attributes.state` | string |  |
| `data[].id` | string |  |
| `data[].type` | string |  |

## Native endpoint

Through the native Steady API, this operation is `GET /plans` (base URL `https://steadyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-plans.md) for the provider-specific parameters and requirements.

