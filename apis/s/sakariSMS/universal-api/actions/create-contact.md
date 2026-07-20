# Sakari SMS: Create Contact

Creates a new contact in Sakari SMS.

```
POST https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mobile.country": "string",
  "mobile.number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mobile.country": "string",
    "mobile.number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `mobile` | object | no |  |
| `mobile.country` | string | yes |  |
| `mobile.number` | string | yes |  |
| `mobile.verified` | date | no |  |
| `mobile.valid` | boolean | no |  |
| `mobile.lineType` | string | no |  |
| `lists[]` | array<object> | no |  |
| `lists.lists[].id` | string | no |  |
| `lists.lists[].name` | string | no |  |
| `lists.lists[].source` | object | no |  |
| `lists.lists[].source.id` | string | no |  |
| `lists.lists[].source.integration` | string | no |  |
| `lists.lists[].source.lastSynced` | string | no |  |
| `lists.lists[].keyword` | string | no |  |
| `updated.by.subSource` | string<object> | no | Determines how existing contacts with matching mobile numbers are treated |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `POST /v1/accounts/:accountId/contacts` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

