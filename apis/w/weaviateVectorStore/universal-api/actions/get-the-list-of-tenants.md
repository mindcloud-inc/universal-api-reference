# Weaviate Vector Store: Get the list of tenants

Retrieves the list of tenants from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-the-list-of-tenants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-the-list-of-tenants?connectionId=$CONNECTION_ID&classname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "classname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-the-list-of-tenants?${params}`, {
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
| `classname` | string | yes | The name of the collection (class) whose tenants to list. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /schema/:className/tenants` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-the-list-of-tenants.md) for the provider-specific parameters and requirements.

