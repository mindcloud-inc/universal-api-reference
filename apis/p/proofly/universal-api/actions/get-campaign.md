# Proofly: Get Campaign

Retrieves a campaign from your Proofly account.

```
GET https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Proofly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | The campaign ID from List Campaigns. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": 1,
      "name": "Ava Chen",
      "settings": {},
      "stats": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Notification creation timestamp |
| `enabled` | boolean | Whether the notification is enabled |
| `id` | number | Notification ID |
| `name` | string | Notification name |
| `settings` | object | Notification settings |
| `stats` | object | Notification statistics |
| `type` | string | Notification type |

## Native endpoint

Through the native Proofly API, this operation is `GET /campaign/:campaignId` (base URL `https://proofly.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

