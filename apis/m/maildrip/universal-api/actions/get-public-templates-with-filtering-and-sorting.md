# Maildrip: Get public templates with filtering and sorting



```
GET https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-public-templates-with-filtering-and-sorting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-public-templates-with-filtering-and-sorting?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-public-templates-with-filtering-and-sorting?${params}`, {
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
| `category` | string | no | Filter by template category |
| `sort` | string | no | Sort order |
| `limit` | number | no |  |
| `skip` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
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
| `items` | array<object> | List of public templates |

## Native endpoint

Through the native Maildrip API, this operation is `GET /api/v1/templates/public` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-public-templates-with-filtering-and-sorting.md) for the provider-specific parameters and requirements.

