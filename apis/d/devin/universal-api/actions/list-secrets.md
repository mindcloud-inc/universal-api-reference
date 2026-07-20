# Devin: List Secrets

Retrieves a list of secrets from Devin.

```
GET https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-secrets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-secrets?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/list-secrets?${params}`, {
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
| `orgId` | string | yes | Devin organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end_cursor": "string",
      "has_next_page": true,
      "items": [
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
| `end_cursor` | string | Cursor for the next page. |
| `has_next_page` | boolean | Whether more results are available. |
| `items` | array<object> | Secrets returned by Devin. |
| `total` | number | Total count when returned by Devin. |

## Native endpoint

Through the native Devin API, this operation is `GET /v3/organizations/:org_id/secrets` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-secrets.md) for the provider-specific parameters and requirements.

