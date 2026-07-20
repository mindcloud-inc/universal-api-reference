# Flotiq: Get Content Object

Retrieves a content object from Flotiq.

```
GET https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-content-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-content-object?connectionId=$CONNECTION_ID&name=Ava%20Chen&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/get-content-object?${params}`, {
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
| `name` | string | yes | The content type name that owns the object. |
| `id` | string | yes | The Flotiq object ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `GET /content/{{name}}/{{id}}` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-object.md) for the provider-specific parameters and requirements.

