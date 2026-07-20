# Buttondown: List Webhook Attempts

Retrieves webhook attempts from Buttondown.

```
GET https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-webhook-attempts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-webhook-attempts?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/list-webhook-attempts?${params}`, {
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
| `id` | string | yes | Webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total number of matching webhook attempts returned by Buttondown. |
| `next` | string | Pagination URL for the next page when Buttondown provides one. |
| `previous` | string | Pagination URL for the previous page when Buttondown provides one. |
| `results` | array<object> | Webhook delivery attempts returned by Buttondown for the selected webhook. |

## Native endpoint

Through the native Buttondown API, this operation is `GET /webhooks/:id/attempts` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-attempts.md) for the provider-specific parameters and requirements.

