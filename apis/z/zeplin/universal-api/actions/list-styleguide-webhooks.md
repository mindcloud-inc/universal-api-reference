# Zeplin: List Styleguide Webhooks

Retrieves a list of styleguide webhooks from Zeplin.

```
GET https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0&styleguideId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "styleguideId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/list-styleguide-webhooks?${params}`, {
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
| `styleguideId` | string | yes | Styleguide id |
| `status` | string | no | Filter by webhook status |
| `urlHealth` | string | no | Filter by health of webhook's URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "created_by": {},
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated": 1,
      "updated_by": {},
      "url": "https://example.com",
      "url_health": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `created_by` | object |  |
| `events` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated` | number |  |
| `updated_by` | object |  |
| `url` | string |  |
| `url_health` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `GET /styleguides/{styleguide_id}/webhooks` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-styleguide-webhooks.md) for the provider-specific parameters and requirements.

