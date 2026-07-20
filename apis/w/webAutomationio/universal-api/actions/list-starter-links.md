# WebAutomation.io: List Starter Links

Lists starter links configured for a specific extractor.

```
GET https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-starter-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebAutomation.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-starter-links?connectionId=$CONNECTION_ID&extractorId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "extractorId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webAutomationio/latest/actions/list-starter-links?${params}`, {
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
| `extractorId` | number | yes | The extractor ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebAutomation.io API returns.

## Native endpoint

Through the native WebAutomation.io API, this operation is `GET /extractors/start_urls/{{EXTRACTOR_ID}}/` (base URL `https://webautomation.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-starter-links.md) for the provider-specific parameters and requirements.

