# Klipfolio: List Klips

Retrieves a list of Klips from Klipfolio.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-klips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-klips?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-klips?${params}`, {
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /klips` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-klips.md) for the provider-specific parameters and requirements.

