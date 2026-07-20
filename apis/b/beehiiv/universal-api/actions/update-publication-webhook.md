# Beehiiv: Update Publication Webhook

Updates a publication webhook in Beehiiv.

```
PUT https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/update-publication-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beehiiv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/update-publication-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicationId": "string",
  "endpointId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/update-publication-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicationId": "string",
    "endpointId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicationId` | string | yes | The prefixed ID of the publication object. |
| `endpointId` | string | yes | The prefixed ID of the webhook object. |
| `event_types[]` | array<string> | no | The types of events the webhook will receive. |
| `description` | string | no | A description of the webhook. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beehiiv API returns.

## Native endpoint

Through the native Beehiiv API, this operation is `PATCH /v2/publications/:publicationId/webhooks/:endpointId` (base URL `https://api.beehiiv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-publication-webhook.md) for the provider-specific parameters and requirements.

