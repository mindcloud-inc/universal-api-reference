# Senja: List Testimonials

Retrieves testimonials from your Senja project.

```
GET https://connect.mindcloud.co/v1/universal/senja/latest/actions/list-testimonials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Senja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/senja/latest/actions/list-testimonials?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/senja/latest/actions/list-testimonials?${params}`, {
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
| `approved` | boolean | no | Filter testimonials by approval status. |
| `integration` | string | no | Filter testimonials by integration. |
| `lang` | string | no | Filter testimonials by language. |
| `rating` | number | no | Filter testimonials by rating. |
| `tags[]` | array<string> | no | Filter testimonials by tag. |
| `type` | string | no | Filter testimonials by type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "testimonials": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `testimonials` | array<object> | Testimonials returned for the current page. |
| `total` | number | Total number of testimonials returned by Senja. |

## Native endpoint

Through the native Senja API, this operation is `GET /testimonials` (base URL `https://api.senja.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-testimonials.md) for the provider-specific parameters and requirements.

