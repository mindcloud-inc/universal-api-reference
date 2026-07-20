# Rossum: List Schemas

Retrieves schemas from Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-schemas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/list-schemas?${params}`, {
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
| `id` | string | no | Filter schemas by ID. |
| `name` | string | no | Filter schemas by name. |
| `ordering` | string | no | Sort schemas by a supported Rossum ordering value. |
| `queue` | string | no | Filter schemas by queue ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "next": {},
        "previous": {}
      },
      "results": [
        {
          "id": 1,
          "modifiedAt": "string",
          "modifiedBy": {},
          "name": "Ava Chen",
          "queues": [
            "string"
          ],
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.next` | object |  |
| `pagination.previous` | object |  |
| `results[].id` | number |  |
| `results[].modifiedAt` | string |  |
| `results[].modifiedBy` | object |  |
| `results[].name` | string |  |
| `results[].queues[]` | string |  |
| `results[].url` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `GET /schemas` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-schemas.md) for the provider-specific parameters and requirements.

