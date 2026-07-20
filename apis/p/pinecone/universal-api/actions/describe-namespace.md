# Pinecone: Describe Namespace

Retrieves details for a namespace from Pinecone.

```
GET https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinecone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-namespace?connectionId=$CONNECTION_ID&namespace=mc-stage3-ns-example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace": "mc-stage3-ns-example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinecone/latest/actions/describe-namespace?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `namespace` | string | yes | The name of the namespace. Example: `mc-stage3-ns-example`. |

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

Through the native Pinecone API, this operation is `GET {{credentials.indexHost}}/namespaces/:namespace` (base URL `https://api.pinecone.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-namespace.md) for the provider-specific parameters and requirements.

