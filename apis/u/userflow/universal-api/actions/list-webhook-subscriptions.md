# Userflow: List Webhook Subscriptions

Retrieves a list of webhook subscriptions from Userflow.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-webhook-subscriptions?${params}`, {
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
| `limit` | number | no | Maximum number of webhook subscriptions to return. |
| `orderBy` | string | no | Sort webhook subscriptions by created_at or url. |
| `startingAfter` | string | no | Return webhook subscriptions after this subscription ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "api_version": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "disabled": true,
          "id": "string",
          "object": "string",
          "secret": "string",
          "topics": [
            "string"
          ],
          "url": "https://example.com"
        }
      ],
      "has_more": true,
      "next_page_url": "https://example.com",
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of webhook subscriptions. |
| `data[].api_version` | string | API version used for the subscription. |
| `data[].created_at` | date | Subscription creation timestamp. |
| `data[].disabled` | boolean | Whether the subscription is disabled. |
| `data[].id` | string | Webhook subscription ID. |
| `data[].object` | string | Returned object type. |
| `data[].secret` | string | Webhook secret when available. |
| `data[].topics` | array<string> | Subscribed webhook topics. |
| `data[].url` | string | Destination URL. |
| `has_more` | boolean | Whether more results are available. |
| `next_page_url` | string | URL for the next page. |
| `object` | string | Response object type. |
| `url` | string | Current page URL. |

## Native endpoint

Through the native Userflow API, this operation is `GET /webhook_subscriptions` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

