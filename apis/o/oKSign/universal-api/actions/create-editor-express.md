# OKSign: Create Editor Express

Creates a new Editor Express session in OKSign.

```
POST https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/create-editor-express
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OKSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/create-editor-express" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/create-editor-express', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "reason": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | string | Editor Express creation result payload. |
| `status` | string |  |

## Native endpoint

Through the native OKSign API, this operation is `POST /editorexpress/create` (base URL `https://www.oksign.be/services/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-editor-express.md) for the provider-specific parameters and requirements.

