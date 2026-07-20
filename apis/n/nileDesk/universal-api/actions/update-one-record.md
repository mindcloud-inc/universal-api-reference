# NileDesk: Update One Record

Updates a single record in NileDesk.

```
PUT https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/update-one-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NileDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/update-one-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": {},
  "filters": {},
  "template_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/update-one-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": {},
    "filters": {},
    "template_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | object | yes | The field values to apply to the matching record. |
| `filters` | object | yes | The NileDesk filter object used to identify the record to update. |
| `template_id` | string | yes | The NileDesk template containing the record to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider message describing the result. |
| `success` | boolean | Whether NileDesk accepted the request. |

## Native endpoint

Through the native NileDesk API, this operation is `POST /UpdateOneRecord` (base URL `https://app.niledesk.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-one-record.md) for the provider-specific parameters and requirements.

