# Nicereply: Get Feedback Object

Retrieves a feedback object from Nicereply.

```
GET https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-feedback-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nicereply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-feedback-object?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/get-feedback-object?${params}`, {
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
| `id` | string | yes | The Nicereply feedback object ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nicereply API returns.

## Native endpoint

Through the native Nicereply API, this operation is `GET /feedback-objects/:id` (base URL `https://api.nicereply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback-object.md) for the provider-specific parameters and requirements.

