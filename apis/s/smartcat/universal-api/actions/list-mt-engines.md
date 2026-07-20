# Smartcat: List MT Engines

Retrieves MT engines available for the Smartcat account.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/list-mt-engines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/list-mt-engines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/list-mt-engines?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Machine translation engine ID |
| `name` | string | Machine translation engine name |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/account/mtengines` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mt-engines.md) for the provider-specific parameters and requirements.

