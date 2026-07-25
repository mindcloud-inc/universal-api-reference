# Weaviate Vector Store: Get roles assigned to a specific group

Retrieves roles assigned to a specific group from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-roles-assigned-to-a-specific-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-roles-assigned-to-a-specific-group?connectionId=$CONNECTION_ID&id=string&grouptype=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "grouptype": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-roles-assigned-to-a-specific-group?${params}`, {
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
| `id` | string | yes | The unique name of the group. |
| `grouptype` | string | yes | The type of the group. |
| `includefullroles` | string | no | If true, the response will include the full role definitions with all associated permissions. If false, only role names are returned. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /authz/groups/:id/roles/:groupType` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-roles-assigned-to-a-specific-group.md) for the provider-specific parameters and requirements.

