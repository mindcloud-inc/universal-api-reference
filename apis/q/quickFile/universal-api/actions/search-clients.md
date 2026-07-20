# QuickFile: Search Clients



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-clients?connectionId=$CONNECTION_ID&limit=25&offset=0&sortBy=CompanyName&sortDirection=ASC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "25",
  "offset": "0",
  "sortBy": "CompanyName",
  "sortDirection": "ASC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-clients?${params}`, {
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
| `companyName` | string | no | Whole or partial client company name |
| `contactName` | string | no | Whole or partial client contact name |
| `email` | string | no | Whole or partial client email address |
| `limit` | number | yes | Maximum number of clients to return Default: `25`. |
| `offset` | number | yes | Page offset for client results Default: `0`. |
| `sortBy` | string | yes | Field used to order client results Default: `CompanyName`. |
| `sortDirection` | string | yes | Direction used to order client results Default: `ASC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "companyName": "Ava Chen",
      "contactName": "Ava Chen",
      "currency": "string",
      "email": "ava@example.com",
      "isArchived": true,
      "telephone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number | QuickFile client identifier. |
| `companyName` | string | Client company name. |
| `contactName` | string | Primary client contact name. |
| `currency` | string | Client currency or pricing currency. |
| `email` | string | Primary client email address. |
| `isArchived` | boolean | Whether the client is archived. |
| `telephone` | string | Primary client telephone number. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /client/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-clients.md) for the provider-specific parameters and requirements.

