# Bulldog-WP: List templates

Retrieves templates from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "codeExpirationMinutes": 1,
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "parameterFormat": "string",
      "permission": 1,
      "rejectedReason": "string",
      "status": "string",
      "subCategory": "string",
      "templateId": "string",
      "waba": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `codeExpirationMinutes` | number |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `parameterFormat` | string |  |
| `permission` | number |  |
| `rejectedReason` | string |  |
| `status` | string |  |
| `subCategory` | string |  |
| `templateId` | string |  |
| `waba` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /waba/templates` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-templates.md) for the provider-specific parameters and requirements.

