# Lunch Money: Get transaction attachment download URL



```
GET https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-transaction-attachment-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunch Money `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-transaction-attachment-url?connectionId=$CONNECTION_ID&file_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lunchMoney/latest/actions/get-transaction-attachment-url?${params}`, {
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
| `file_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Lunch Money API, this operation is `GET /transactions/attachments/:file_id` (base URL `https://api.lunchmoney.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-attachment-url.md) for the provider-specific parameters and requirements.

