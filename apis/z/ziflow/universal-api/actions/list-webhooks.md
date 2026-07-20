# Ziflow: List Webhooks

Retrieves webhook subscriptions from your Ziflow account.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "subscription_types": {
        "proof": {
          "all": true,
          "changed": true,
          "comment": true,
          "comment_reaction": true,
          "complete_review": true,
          "created": true,
          "decision": true,
          "deleted": true,
          "first_opened": true,
          "mentions": true,
          "processed": true,
          "restored": true,
          "shared": true,
          "stage_deadline_passed": true,
          "stage_locked": true,
          "stage_started": true,
          "status_change": true,
          "summary": true
        }
      },
      "target": "string",
      "webhook_signature_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created_at` | string |  |
| `id` | string |  |
| `name` | string |  |
| `subscription_types.proof.all` | boolean |  |
| `subscription_types.proof.changed` | boolean |  |
| `subscription_types.proof.comment` | boolean |  |
| `subscription_types.proof.comment_reaction` | boolean |  |
| `subscription_types.proof.complete_review` | boolean |  |
| `subscription_types.proof.created` | boolean |  |
| `subscription_types.proof.decision` | boolean |  |
| `subscription_types.proof.deleted` | boolean |  |
| `subscription_types.proof.first_opened` | boolean |  |
| `subscription_types.proof.mentions` | boolean |  |
| `subscription_types.proof.processed` | boolean |  |
| `subscription_types.proof.restored` | boolean |  |
| `subscription_types.proof.shared` | boolean |  |
| `subscription_types.proof.stage_deadline_passed` | boolean |  |
| `subscription_types.proof.stage_locked` | boolean |  |
| `subscription_types.proof.stage_started` | boolean |  |
| `subscription_types.proof.status_change` | boolean |  |
| `subscription_types.proof.summary` | boolean |  |
| `target` | string |  |
| `webhook_signature_key` | string |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /webhooks` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

