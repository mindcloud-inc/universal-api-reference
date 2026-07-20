# Implisense: Get Company Data

Retrieves company data from Implisense API.

```
GET https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Implisense `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-data?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/implisenseAPI/latest/actions/get-company-data?${params}`, {
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
| `id` | string | yes | Implisense company identifier, for example DEVFCLQFW054. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "capital": "string",
      "city": "string",
      "email": "ava@example.com",
      "employees": {},
      "externalIds": {},
      "foundingDate": 1,
      "geo": {},
      "historicalNames": [
        "Ava Chen"
      ],
      "id": "string",
      "industries": {},
      "legalForm": "string",
      "name": "Ava Chen",
      "phone": "string",
      "profile": "string",
      "purpose": "string",
      "representation": "string",
      "size": {},
      "snippets": [
        {}
      ],
      "socialMedia": [
        {}
      ],
      "statutorySeat": "string",
      "street": "string",
      "timestamp": 1,
      "url": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `capital` | string |  |
| `city` | string |  |
| `email` | string |  |
| `employees` | object |  |
| `externalIds` | object |  |
| `foundingDate` | number |  |
| `geo` | object |  |
| `historicalNames` | array<string> |  |
| `id` | string |  |
| `industries` | object |  |
| `legalForm` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `profile` | string |  |
| `purpose` | string |  |
| `representation` | string |  |
| `size` | object |  |
| `snippets` | array<object> |  |
| `socialMedia` | array<object> |  |
| `statutorySeat` | string |  |
| `street` | string |  |
| `timestamp` | number |  |
| `url` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native Implisense API, this operation is `GET /companies/:id/data` (base URL `https://german-company-data.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-data.md) for the provider-specific parameters and requirements.

