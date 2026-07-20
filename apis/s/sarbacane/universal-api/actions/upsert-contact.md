# Sarbacane: Upsert Contact

Finds a contact in Sarbacane, or creates one if needed.

```
PUT https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/upsert-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/upsert-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/upsert-contact', {
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
| `email` | string | no | Contact email address. |
| `listId` | string | no | Sarbacane list ID. |
| `phone` | string | no | Contact phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | array<string> | Upserted contact tuple returned by Sarbacane. |

## Native endpoint

Through the native Sarbacane API, this operation is `POST /lists/{listId}/contacts/upsert` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-contact.md) for the provider-specific parameters and requirements.

