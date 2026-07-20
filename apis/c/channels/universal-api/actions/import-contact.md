# Channels: Import Contact

Imports a contact into Channels.

```
POST https://connect.mindcloud.co/v1/universal/channels/latest/actions/import-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/import-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "details": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/import-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "details": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `details` | object | yes | Contact details object matching your Channels contact structure. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternativeMsisdns": [
        "string"
      ],
      "company": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "externalLink": "https://example.com",
      "externalOrderLink": "https://example.com",
      "externalServices": {
        "recordId": 1
      },
      "firstName": "Ava",
      "id": 1,
      "lastModificationDate": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternativeMsisdns[]` | string |  |
| `company` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `externalLink` | string |  |
| `externalOrderLink` | string |  |
| `externalServices.recordId` | number |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastModificationDate` | date |  |
| `lastName` | string |  |
| `source` | string |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/contacts` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-contact.md) for the provider-specific parameters and requirements.

