# Paradym: List Trusted Entities

Retrieves a list of trusted entities from Paradym.

```
GET https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-trusted-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paradym `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-trusted-entities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paradym/latest/actions/list-trusted-entities?${params}`, {
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
| `name` | string | no | Search trusted entities by name. Example: `Trustland Government`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "page": {
          "maxSize": "string",
          "size": "string"
        },
        "sort": [
          {
            "id": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.page.maxSize` | string |  |
| `meta.page.size` | string |  |
| `meta.sort[].id` | string |  |

## Native endpoint

Through the native Paradym API, this operation is `GET /projects/:projectId/trusted-entities` (base URL `https://api.paradym.id/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-trusted-entities.md) for the provider-specific parameters and requirements.

