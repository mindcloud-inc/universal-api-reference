# Harvest: Retrieve Contact

Retrieves a contact from Harvest.

```
GET https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-contact?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "phoneMobile": "string",
      "phoneOffice": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `createdAt` | date |  |
| `email` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phoneMobile` | string |  |
| `phoneOffice` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `GET /v2/contacts/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

