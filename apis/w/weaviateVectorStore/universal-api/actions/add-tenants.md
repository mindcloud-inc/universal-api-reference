# Weaviate Vector Store: Add Tenants

Creates a new tenant in Weaviate.

```
POST https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/add-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/add-tenants" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "className": "Ava Chen",
  "tenants[0].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/add-tenants', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "className": "Ava Chen",
    "tenants[0].name": "Ava Chen"
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
| `tenants[0].activityStatus` | string | no | Default: `ACTIVE`. |

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

Through the native Weaviate Vector Store API, this operation is `POST /v1/schema/:className/tenants` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tenants.md) for the provider-specific parameters and requirements.

