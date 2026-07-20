# Calendly: List Webhook Subscriptions

Retrieves webhook subscriptions from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-webhook-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-webhook-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0&organization=https%3A%2F%2Fapi.calendly.com%2Forganizations%2Fe684df12-9454-43ef-8fc4-2d0faa4ec21e&scope=organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organization": "https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e",
  "scope": "organization"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-webhook-subscriptions?${params}`, {
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
| `organization` | list | yes | Organization URI filter. One of: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. Default: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `scope` | list | yes | Scope for webhook subscription lookup. One of: `organization`, `user`. Default: `organization`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> | Webhook subscription records. |
| `pagination` | object | Pagination metadata for webhook subscriptions. |

## Native endpoint

Through the native Calendly API, this operation is `GET /webhook_subscriptions` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhook-subscriptions.md) for the provider-specific parameters and requirements.

