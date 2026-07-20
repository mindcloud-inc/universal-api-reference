# Nightfall.ai: Annotate Finding

Updates a finding annotation in Nightfall.ai.

```
PUT https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/annotate-finding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/annotate-finding" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "findingId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/annotate-finding', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "findingId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `findingId` | string | yes | The UUID of the finding to annotate. |
| `type` | string | yes | Annotation type to apply. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nightfall.ai API returns.

## Native endpoint

Through the native Nightfall.ai API, this operation is `POST /dlp/v1/findings/:findingId/annotate` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/annotate-finding.md) for the provider-specific parameters and requirements.

