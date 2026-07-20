# Blueink: List Bundle Events

Retrieves event history for a Blueink bundle.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundle-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundle-events?connectionId=$CONNECTION_ID&bundleSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bundleSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundle-events?${params}`, {
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
| `bundleSlug` | string | yes | Bundle slug to inspect events for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "kind": "string",
      "packetId": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `kind` | string |  |
| `packetId` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /bundles/:bundleSlug/events/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bundle-events.md) for the provider-specific parameters and requirements.

