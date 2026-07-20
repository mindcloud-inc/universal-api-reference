# Ventrata: List Capabilities

Retrieves capabilities from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-capabilities?${params}`, {
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
      "dependencies": [
        "string"
      ],
      "docs": "string",
      "id": "string",
      "required": true,
      "revision": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dependencies[]` | string |  |
| `docs` | string |  |
| `id` | string |  |
| `required` | boolean |  |
| `revision` | number |  |

## Native endpoint

Through the native Ventrata API, this operation is `GET octo/capabilities` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-capabilities.md) for the provider-specific parameters and requirements.

