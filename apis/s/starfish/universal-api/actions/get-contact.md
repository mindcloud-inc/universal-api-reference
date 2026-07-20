# Starfish: Get Contact

Retrieves a specific contact from Starfish.

```
GET https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starfish `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starfish/latest/actions/get-contact?${params}`, {
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
      "address": "string",
      "addressNumber": "string",
      "adminId": 1,
      "birthday": "2026-05-07T12:00:00.000Z",
      "chainId": 1,
      "city": "string",
      "company": "string",
      "contactId": 1,
      "contactUid": "string",
      "country": "string",
      "countryOrigin": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "idIssueCountry": "string",
      "idNr": "string",
      "idType": "string",
      "invoices": [
        {}
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "location": [
        {}
      ],
      "meta": [
        {}
      ],
      "name": "Ava Chen",
      "nationality": "string",
      "phone": "string",
      "phoneMobile": "string",
      "reservations": [
        {}
      ],
      "state": "string",
      "status": "string",
      "type": "string",
      "vatNumber": "string",
      "zipcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressNumber` | string |  |
| `adminId` | number |  |
| `birthday` | date |  |
| `chainId` | number |  |
| `city` | string |  |
| `company` | string |  |
| `contactId` | number |  |
| `contactUid` | string |  |
| `country` | string |  |
| `countryOrigin` | string |  |
| `created` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `idIssueCountry` | string |  |
| `idNr` | string |  |
| `idType` | string |  |
| `invoices` | array<object> |  |
| `lastModified` | date |  |
| `lastName` | string |  |
| `location` | array<object> |  |
| `meta` | array<object> |  |
| `name` | string |  |
| `nationality` | string |  |
| `phone` | string |  |
| `phoneMobile` | string |  |
| `reservations` | array<object> |  |
| `state` | string |  |
| `status` | string |  |
| `type` | string |  |
| `vatNumber` | string |  |
| `zipcode` | string |  |

## Native endpoint

Through the native Starfish API, this operation is `GET /contacts/:contact_id` (base URL `https://api.camping.care/v21`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

