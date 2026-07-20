# Maildroppa: Upsert Subscriber Field By ID



```
PUT https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/upsert-subscriber-field-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/upsert-subscriber-field-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/upsert-subscriber-field-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldTypeId` | string | no | Unique identifier of the field type. |
| `subscriberId` | string | no | Unique identifier of the subscriber. |
| `value` | string | no | New or updated value for the specified subscriber field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldTypeId": "string",
      "subscriberId": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fieldTypeId` | string | Unique identifier of the field type. |
| `subscriberId` | string | Unique identifier of the subscriber. |
| `value` | string | New or updated value for the specified subscriber field. |

## Native endpoint

Through the native Maildroppa API, this operation is `POST /subscribers/fields/by-id` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-subscriber-field-by-id.md) for the provider-specific parameters and requirements.

