# Claid AI: List Storages

Retrieves connected storages from Claid AI.

```
GET https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/list-storages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/list-storages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/list-storages?${params}`, {
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
      "id": 1,
      "name": "Ava Chen",
      "parameters": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Storage identifier. |
| `name` | string | Storage name in Claid. |
| `parameters` | object | Connector-specific storage parameters. |
| `type` | string | Storage connector type. |

## Native endpoint

Through the native Claid AI API, this operation is `GET storage/storages` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-storages.md) for the provider-specific parameters and requirements.

