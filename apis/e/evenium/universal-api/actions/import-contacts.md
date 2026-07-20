# Evenium: Import Contacts

Imports contacts into Evenium.

```
PUT https://connect.mindcloud.co/v1/universal/evenium/latest/actions/import-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/import-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/evenium/latest/actions/import-contacts', {
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
| `contacts` | string | no | Contacts payload for bulk import. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "error": 1,
      "messages": [
        {}
      ],
      "processed": 1,
      "status": "string",
      "warning": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Number of created records. |
| `error` | number | Number of error records. |
| `messages` | array<object> | Per-record import messages. |
| `processed` | number | Number of processed records. |
| `status` | string | Overall import status. |
| `warning` | number | Number of warning records. |

## Native endpoint

Through the native Evenium API, this operation is `PUT /contacts` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contacts.md) for the provider-specific parameters and requirements.

