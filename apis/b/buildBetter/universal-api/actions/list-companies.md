# BuildBetter: List Companies



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-companies?${params}`, {
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
| `limit` | number | no | Maximum number of companies to return. Default: `25`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "photo_url": "https://example.com",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Company color value. |
| `domain` | string | Company website domain. |
| `id` | string | BuildBetter company identifier. |
| `name` | string | Company name. |
| `photo_url` | string | Company logo or photo URL. |
| `updated_at` | date | Last updated timestamp. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

