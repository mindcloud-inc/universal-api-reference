# Weaviate Vector Store: Update Tenants

Updates a tenant in Weaviate.

```
PUT https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/update-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/update-tenants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "className": "Ava Chen",
  "tenants[0].name": "Ava Chen",
  "tenants[0].activityStatus": "HOT"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/update-tenants', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "className": "Ava Chen",
    "tenants[0].name": "Ava Chen",
    "tenants[0].activityStatus": "HOT"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `className` | string | yes |  |
| `tenants[0].name` | string | yes |  |
| `tenants[0].activityStatus` | string | yes | Default: `HOT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityStatus": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityStatus` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `PUT /v1/schema/:className/tenants` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tenants.md) for the provider-specific parameters and requirements.

