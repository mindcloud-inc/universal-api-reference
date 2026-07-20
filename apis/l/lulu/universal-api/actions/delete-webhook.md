# Lulu: Delete Webhook

Deletes an existing webhook from Lulu.

```
DELETE https://connect.mindcloud.co/v1/universal/lulu/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lulu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lulu/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&id=6b522ab9-31ec-4418-a904-95436160d4a8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "6b522ab9-31ec-4418-a904-95436160d4a8"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lulu/latest/actions/delete-webhook?${params}`, {
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
| `id` | string | yes | Lulu webhook ID. Default: `6b522ab9-31ec-4418-a904-95436160d4a8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean | Synthetic confirmation field used to satisfy validator requirements for Lulu's 204 delete response. |

## Native endpoint

Through the native Lulu API, this operation is `DELETE /webhooks/{id}/` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

