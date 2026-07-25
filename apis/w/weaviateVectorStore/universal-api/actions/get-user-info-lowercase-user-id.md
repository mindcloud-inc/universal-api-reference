# Weaviate Vector Store: Get User Info (Lowercase User ID)

Retrieves user info from Weaviate.

```
GET https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-user-info-lowercase-user-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-user-info-lowercase-user-id?connectionId=$CONNECTION_ID&userid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/get-user-info-lowercase-user-id?${params}`, {
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
| `userid` | string | yes | The name of the user. |
| `includelastusedtime` | string | no | Whether to include the last used time of the given user |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Weaviate Vector Store API returns.

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `GET /users/db/:user_id` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info-lowercase-user-id.md) for the provider-specific parameters and requirements.

