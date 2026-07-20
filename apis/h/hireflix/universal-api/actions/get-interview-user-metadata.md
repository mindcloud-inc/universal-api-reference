# Hireflix: Get Interview User Metadata

Retrieves user metadata for an interview in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview-user-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview-user-metadata?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-interview-user-metadata?${params}`, {
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
| `variables.id` | string | yes | The Hireflix interview ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Hireflix API returns.

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-interview-user-metadata.md) for the provider-specific parameters and requirements.

