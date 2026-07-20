# Auphonic: Delete Production Webhook

Deletes a production webhook from Auphonic.

```
DELETE https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/delete-production-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Auphonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/delete-production-webhook?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/auphonic/latest/actions/delete-production-webhook?${params}`, {
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
| `uuid` | string | yes | UUID of the production. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhook": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhook` | string |  |

## Native endpoint

Through the native Auphonic API, this operation is `DELETE /production/:uuid/webhook.json` (base URL `https://auphonic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-production-webhook.md) for the provider-specific parameters and requirements.

