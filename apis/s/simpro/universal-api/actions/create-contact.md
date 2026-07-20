# Simpro: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "0",
  "GivenName": "Morgan"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpro/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "0",
    "GivenName": "Morgan"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Simpro company ID. Single-company builds usually use 0. Default: `0`. Example: `0`. |
| `GivenName` | string | yes | Contact first name. Example: `Morgan`. |
| `FamilyName` | string | no | Contact last name. Example: `Reed`. |
| `Email` | string | no | Contact email address. Example: `morgan.reed@example.com`. |
| `CellPhone` | string | no | Contact mobile phone. Example: `+1 415 555 0133`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "altPhone": "string",
      "cellPhone": "string",
      "dateModified": "string",
      "department": "string",
      "email": "ava@example.com",
      "familyName": "Ava Chen",
      "fax": "string",
      "givenName": "Ava Chen",
      "id": 1,
      "notes": "string",
      "position": "string",
      "title": "string",
      "workPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altPhone` | string |  |
| `cellPhone` | string |  |
| `dateModified` | string |  |
| `department` | string |  |
| `email` | string |  |
| `familyName` | string |  |
| `fax` | string |  |
| `givenName` | string |  |
| `id` | number |  |
| `notes` | string |  |
| `position` | string |  |
| `title` | string |  |
| `workPhone` | string |  |

## Native endpoint

Through the native Simpro API, this operation is `POST /companies/:companyId/contacts/` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

