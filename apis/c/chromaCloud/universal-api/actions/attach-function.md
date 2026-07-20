# Chroma Cloud: Attach function

Attaches a function to a collection in Chroma Cloud.

```
POST https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/attach-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/attach-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "name": "Ava Chen",
  "functionId": "string",
  "outputCollection": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/attach-function', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "name": "Ava Chen",
    "functionId": "string",
    "outputCollection": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | Collection UUID. |
| `name` | string | yes |  |
| `functionId` | string | yes |  |
| `outputCollection` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attached_function": {},
      "created": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attached_function` | object |  |
| `created` | boolean |  |

## Native endpoint

Through the native Chroma Cloud API, this operation is `POST /api/v2/tenants/:tenant/databases/:database/collections/:collection_id/functions/attach` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-function.md) for the provider-specific parameters and requirements.

