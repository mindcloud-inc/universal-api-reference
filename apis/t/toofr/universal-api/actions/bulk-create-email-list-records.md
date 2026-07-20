# Toofr: Bulk Create Email List Records

Creates multiple email list records in Toofr.

```
POST https://connect.mindcloud.co/v1/universal/toofr/latest/actions/bulk-create-email-list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/bulk-create-email-list-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "records": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toofr/latest/actions/bulk-create-email-list-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "records": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Email list ID. |
| `records` | string | yes | JSON array or encoded records payload to bulk create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "errors": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `errors` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `POST /lists/:list_id/list_records/bulk_list_records` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-email-list-records.md) for the provider-specific parameters and requirements.

