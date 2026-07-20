# ProdPad: Get Idea

Retrieves an idea from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/get-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/get-idea?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/get-idea?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {
        "id": 1,
        "name": "Ava Chen",
        "slug": "string"
      },
      "actual_outcomes": "string",
      "confidence": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator": {
        "display_name": "Ava Chen",
        "id": 1,
        "username": "Ava Chen"
      },
      "description": "string",
      "engagement": 1,
      "id": 1,
      "impact": 1,
      "popularity": 1,
      "project_id": 1,
      "source": "string",
      "state": "string",
      "target_outcomes": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "web_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account.id` | number |  |
| `account.name` | string |  |
| `account.slug` | string |  |
| `actual_outcomes` | string |  |
| `confidence` | string |  |
| `created_at` | date |  |
| `creator.display_name` | string |  |
| `creator.id` | number |  |
| `creator.username` | string |  |
| `description` | string |  |
| `engagement` | number |  |
| `id` | number |  |
| `impact` | number |  |
| `popularity` | number |  |
| `project_id` | number |  |
| `source` | string |  |
| `state` | string |  |
| `target_outcomes` | string |  |
| `title` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |
| `web_url` | string |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /ideas/:id` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-idea.md) for the provider-specific parameters and requirements.

