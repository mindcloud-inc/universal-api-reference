# Pinecone: Create Namespace

Creates a namespace in a Pinecone index.

```
POST https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-namespace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "mc-stage3-ns-example"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/create-namespace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "mc-stage3-ns-example"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of the namespace. Example: `mc-stage3-ns-example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "record_count": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `record_count` | string |  |

## Native endpoint

Through the native Pinecone API, this operation is `POST {{credentials.indexHost}}/namespaces` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-namespace.md) for the provider-specific parameters and requirements.

