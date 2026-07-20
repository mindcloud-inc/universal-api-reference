# Ubiqod by Skiply: List Interfaces



```
GET https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-interfaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ubiqod by Skiply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-interfaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ubiqodBySkiply/latest/actions/list-interfaces?${params}`, {
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
      "id": "string",
      "interactionSubtype": "string",
      "interactionType": "string",
      "label": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Interface ID. |
| `interactionSubtype` | string | Interaction subtype. |
| `interactionType` | string | Interaction type. |
| `label` | string | Interface label. |

## Native endpoint

Through the native Ubiqod by Skiply API, this operation is `GET /interfaces` (base URL `https://api.ubiqod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-interfaces.md) for the provider-specific parameters and requirements.

