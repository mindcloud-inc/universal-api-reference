# Timely: List Webhooks

Retrieves webhooks from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-webhooks?${params}`, {
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
| `accountId` | number | yes | Account ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of webhooks to return Default: `100`. |
| `offset` | number | no | Number of webhooks to skip Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "active": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_headers": {},
      "id": 1,
      "secret_token": "string",
      "subscriptions": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `active` | boolean |  |
| `created_at` | date |  |
| `custom_headers` | object |  |
| `id` | number |  |
| `secret_token` | string |  |
| `subscriptions` | array<string> |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/webhooks` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

