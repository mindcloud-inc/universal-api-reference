# Geral: Get Link

Retrieves a link from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-link?connectionId=$CONNECTION_ID&linkId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-link?${params}`, {
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
| `linkId` | number | yes | The link ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clicks": 1,
      "datetime": "2026-05-07T12:00:00.000Z",
      "domain_id": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "location_url": "https://example.com",
      "order": 1,
      "project_id": 1,
      "settings": {},
      "start_date": "2026-05-07T12:00:00.000Z",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clicks` | number | Click count. |
| `datetime` | date | Creation timestamp. |
| `domain_id` | number | Domain ID. |
| `end_date` | date | Optional end date. |
| `id` | number | Link ID. |
| `location_url` | string | Destination URL. |
| `order` | number | Sort order. |
| `project_id` | number | Project ID. |
| `settings` | object | Link settings. |
| `start_date` | date | Optional start date. |
| `type` | string | Link type. |
| `url` | string | Short link URL slug. |

## Native endpoint

Through the native Geral API, this operation is `GET /links/:link_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link.md) for the provider-specific parameters and requirements.

