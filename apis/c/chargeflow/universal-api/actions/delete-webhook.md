# Chargeflow: Delete Webhook

Deletes an existing webhook from Chargeflow.

```
DELETE https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/delete-webhook?${params}`, {
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
| `id` | string | yes | The Chargeflow webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Chargeflow API, this operation is `DELETE /webhooks/{id}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

