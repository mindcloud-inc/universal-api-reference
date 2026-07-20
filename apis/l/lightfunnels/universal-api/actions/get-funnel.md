# Lightfunnels: Get Funnel



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-funnel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-funnel?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/get-funnel?${params}`, {
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
      "node": {
        "id": "string",
        "name": "Ava Chen",
        "published": true,
        "slug": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `node` | object | Funnel node. |
| `node.id` | string | Funnel id. |
| `node.name` | string | Funnel name. |
| `node.published` | boolean | Whether the funnel is published. |
| `node.slug` | string | Funnel slug. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-funnel.md) for the provider-specific parameters and requirements.

