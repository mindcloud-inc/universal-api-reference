# LaunchNotes: Get Node



```
GET https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LaunchNotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-node?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launchNotes/latest/actions/get-node?${params}`, {
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
| `id` | string | yes | Node identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__typename": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__typename` | string | GraphQL node type name. |
| `id` | string | Node identifier. |

## Native endpoint

Through the native LaunchNotes API, this operation is `POST /graphql` (base URL `https://app.launchnotes.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-node.md) for the provider-specific parameters and requirements.

