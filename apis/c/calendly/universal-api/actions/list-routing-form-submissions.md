# Calendly: List Routing Form Submissions

Retrieves routing form submissions from Calendly.

```
GET https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-routing-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-routing-form-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&routingForm=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "routingForm": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-routing-form-submissions?${params}`, {
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
| `routingForm` | string | yes | Routing form URI filter. |
| `sort` | list | no | Sort order for routing form submissions. One of: `created_at:asc`, `created_at:desc`. |

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
| `collection` | array<object> | Routing form submission records. |
| `pagination` | object | Pagination metadata for routing form submissions. |

## Native endpoint

Through the native Calendly API, this operation is `GET /routing_form_submissions` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-routing-form-submissions.md) for the provider-specific parameters and requirements.

