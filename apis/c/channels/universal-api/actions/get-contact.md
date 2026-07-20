# Channels: Get Contact

Retrieves a contact from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/get-contact?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Contact ID. |

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

Through the native Channels API, this operation is `GET /api/v1/contacts/{contactId}` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

