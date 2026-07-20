# Feathery: List Form Submissions



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-form-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-form-submissions?connectionId=$CONNECTION_ID&form_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-form-submissions?${params}`, {
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
| `form_id` | string | yes | The ID of the form to get submission data for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_time` | date | no | Limit submissions to after this update time. |
| `end_time` | date | no | Limit submissions to before this update time. |
| `created_after` | date | no | Limit submissions to after this creation time. |
| `created_before` | date | no | Limit submissions to before this creation time. |
| `count` | number | no | Limit the number of returned submissions. |
| `completed` | boolean | no | Only fetch submissions that are either completed or incomplete. |
| `field_search` | string | no | Stringified JSON array of field-value match objects. |
| `fuzzy_search` | string | no | Stringified JSON object describing fuzzy search options. |
| `fields` | string | no | Comma-separated list of field IDs to include in the response. |
| `no_field_values` | boolean | no | If true, do not return field data. |
| `sort` | string | no | Sort returned field values, for example by layout. |
| `page_size` | number | no | Maximum number of submissions to return in one page. |
| `use_cache` | boolean | no | If true, fetch results from the cached source for lower latency. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "current_page": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ],
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `current_page` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/form/submission/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-submissions.md) for the provider-specific parameters and requirements.

