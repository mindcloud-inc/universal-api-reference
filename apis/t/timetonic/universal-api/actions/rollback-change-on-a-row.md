# Timetonic: Rollback Change On A Row

Rolls back a row change in Timetonic.

```
PUT https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/rollback-change-on-a-row
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/rollback-change-on-a-row" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bookOwner": "mindcloud",
  "rowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/rollback-change-on-a-row', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bookOwner": "mindcloud",
    "rowId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookOwner` | string | yes | Default: `mindcloud`. |
| `categoryId` | string | no |  |
| `rowId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "req": "string",
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string |  |
| `req` | string |  |
| `status` | string |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rollback-change-on-a-row.md) for the provider-specific parameters and requirements.

