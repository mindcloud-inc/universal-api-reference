# Simpro: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-contact?connectionId=$CONNECTION_ID&companyId=0&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0",
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/get-contact?${params}`, {
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
| `companyId` | number | yes | Simpro company ID. Single-company builds usually use 0. Default: `0`. Example: `0`. |
| `contactId` | number | yes | Contact ID. Example: `1`. |

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

Through the native Simpro API, this operation is `GET /companies/:companyId/contacts/:contactId` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

