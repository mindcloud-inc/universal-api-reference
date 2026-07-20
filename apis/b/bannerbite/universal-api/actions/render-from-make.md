# Bannerbite: Render From Make

Creates a Make render job in Bannerbite.

```
POST https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/render-from-make
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/render-from-make" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobs": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/render-from-make', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobs": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobs` | object<object> | yes | Single Bannerbite Make render job object. Live tenant validation shows this endpoint accepts one object body for a successful render request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Bannerbite API, this operation is `POST /api/integromat/render` (base URL `https://api.bannerbite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-from-make.md) for the provider-specific parameters and requirements.

