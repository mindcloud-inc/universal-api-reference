# timeBuzzer: List Layers



```
GET https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/list-layers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a timeBuzzer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/list-layers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeBuzzer/latest/actions/list-layers?${params}`, {
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
      "child": 1,
      "id": 1,
      "index": 1,
      "name": "Ava Chen",
      "parent": 1,
      "template": 1,
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `child` | number | Child layer ID when present. |
| `id` | number | Layer ID. |
| `index` | number | Layer ordering index. |
| `name` | string | Layer name. |
| `parent` | number | Parent layer ID when present. |
| `template` | number | Template ID. |
| `visible` | boolean | Whether the layer is visible. |

## Native endpoint

Through the native timeBuzzer API, this operation is `GET /open-api/layers` (base URL `https://my.timebuzzer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-layers.md) for the provider-specific parameters and requirements.

