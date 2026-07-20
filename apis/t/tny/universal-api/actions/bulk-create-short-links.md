# Tny: Bulk Create Short Links

Creates multiple shortened links in Tny.

```
POST https://connect.mindcloud.co/v1/universal/tny/latest/actions/bulk-create-short-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tny `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tny/latest/actions/bulk-create-short-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tny/latest/actions/bulk-create-short-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `links` | list<object> | yes | Array of link objects to create. Each item requires url and can include customSlug and domain_id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "errors": [
        {}
      ],
      "failed": 1,
      "results": [
        {}
      ],
      "success": true,
      "tier": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Number of links created successfully. |
| `errors` | array<object> | Per-item errors returned by Tny. |
| `failed` | number | Number of links that failed. |
| `results` | array<object> | Created links returned by Tny. |
| `success` | boolean | Whether the bulk request was accepted. |
| `tier` | string | Plan tier reported by Tny. |
| `total` | number | Total links submitted in the batch. |

## Native endpoint

Through the native Tny API, this operation is `POST /api/v1/shorten/bulk` (base URL `https://www.tny.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-short-links.md) for the provider-specific parameters and requirements.

