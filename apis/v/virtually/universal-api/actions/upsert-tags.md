# Virtually: Upsert Tags

Creates or updates tags in Virtually.

```
PUT https://connect.mindcloud.co/v1/universal/virtually/latest/actions/upsert-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/upsert-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tags[]": [
    {}
  ],
  "tags[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/virtually/latest/actions/upsert-tags', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tags[]": [{}],
    "tags[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags[]` | array<object> | yes | Tags to create or update. |
| `tags[].name` | string | yes | The tag name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags[]` | array<object> | The upserted tags. |
| `tags[].id` | string | The tag ID. |
| `tags[].name` | string | The tag name. |

## Native endpoint

Through the native Virtually API, this operation is `PUT /api/v2/orgs/:orgId/tags` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-tags.md) for the provider-specific parameters and requirements.

