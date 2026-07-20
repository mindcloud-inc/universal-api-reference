# Eduzz: Get Webhook Event Sample

Retrieves a sample payload for an Eduzz webhook event.

```
GET https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-webhook-event-sample
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eduzz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-webhook-event-sample?connectionId=$CONNECTION_ID&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eduzz/latest/actions/get-webhook-event-sample?${params}`, {
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
| `event` | string | yes | Nome do evento. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eduzz API returns.

## Native endpoint

Through the native Eduzz API, this operation is `GET /webhook/v1/origin/sample/:event` (base URL `https://api.eduzz.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-event-sample.md) for the provider-specific parameters and requirements.

