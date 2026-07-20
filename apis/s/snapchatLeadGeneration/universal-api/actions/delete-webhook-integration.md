# Snapchat Lead Generation: Delete Webhook Integration

Deletes a webhook integration from Snapchat Lead Generation.

```
DELETE https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/delete-webhook-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snapchat Lead Generation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/delete-webhook-integration?connectionId=$CONNECTION_ID&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snapchatLeadGeneration/latest/actions/delete-webhook-integration?${params}`, {
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
| `integrationId` | string | yes | The Snapchat webhook integration ID to delete. |

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

Through the native Snapchat Lead Generation API, this operation is `DELETE /lead_gen/integrations/:integrationId` (base URL `https://adsapi.snapchat.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-integration.md) for the provider-specific parameters and requirements.

