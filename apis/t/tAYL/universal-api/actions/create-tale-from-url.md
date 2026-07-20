# TAYL: Create Tale From URL



```
POST https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TAYL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tAYL/latest/actions/create-tale-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public webpage URL to convert into a TAYL tale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {},
      "taleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata` | object |  |
| `taleId` | string |  |

## Native endpoint

Through the native TAYL API, this operation is `POST /submit` (base URL `https://x.tayl.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tale-from-url.md) for the provider-specific parameters and requirements.

