# Snapchat Lead Generation: Send Test Lead Data

Sends test lead data in Snapchat Lead Generation.

```
POST https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/send-test-lead-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/send-test-lead-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "integrationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/send-test-lead-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "integrationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `integrationId` | string | yes | The Snapchat webhook integration ID to send test lead data through. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request_id": "string",
      "request_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request_id` | string |  |
| `request_status` | string |  |

## Native endpoint

Through the native Snapchat Lead Generation API, this operation is `GET /lead_gen/integrations/:integrationId/test` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-test-lead-data.md) for the provider-specific parameters and requirements.

