# Blaze AI: Delete Published Doc Subscription

Deletes an existing published document subscription from Blaze AI.

```
DELETE https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/delete-published-doc-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blaze AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/delete-published-doc-subscription?connectionId=$CONNECTION_ID&workspace_id=994619&id=1166" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspace_id": "994619",
  "id": "1166"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/delete-published-doc-subscription?${params}`, {
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
| `workspace_id` | number | yes | Default: `994619`. |
| `id` | number | yes | Default: `1166`. |

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

Through the native Blaze AI API, this operation is `DELETE /api/v1/w/:workspace_id/published_doc_subscriptions/:id` (base URL `https://api.blaze.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-published-doc-subscription.md) for the provider-specific parameters and requirements.

