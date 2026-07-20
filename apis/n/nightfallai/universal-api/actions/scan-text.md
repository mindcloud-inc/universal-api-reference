# Nightfall.ai: Scan Text

Scans text for sensitive data with Nightfall.ai.

```
POST https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/scan-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/scan-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload[]": [
    "string"
  ],
  "policy": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/scan-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload[]": ["string"],
    "policy": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payload[]` | array<string> | yes | Array of text strings to scan. |
| `policy` | object | yes | Inline Nightfall policy object with detectionRules or referenced detection rule UUIDs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "findings": [
        {}
      ],
      "redactedPayload": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `findings` | array<object> | Arrays of Nightfall findings for each payload item. |
| `redactedPayload` | array<string> | Redacted payload strings in input order. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `POST /v3/scan` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-text.md) for the provider-specific parameters and requirements.

