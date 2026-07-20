# Galileo: Get Integration Status

Retrieves status for a Galileo integration.

```
GET https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-integration-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Galileo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-integration-status?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/galileo/latest/actions/get-integration-status?${params}`, {
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
| `name` | string | yes | Integration name from Galileo, for example openai or anthropic. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Galileo API returns.

## Native endpoint

Through the native Galileo API, this operation is `GET /v2/integrations/:name/status` (base URL `https://api.galileo.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-status.md) for the provider-specific parameters and requirements.

