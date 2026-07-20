# serviceminder.io: Search Contacts

Finds contacts in ServiceMinder by name, email, phone, or address.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/search-contacts?${params}`, {
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
| `addressSearch` | string | no | Search contacts by address. |
| `emailSearch` | string | no | Search contacts by email. |
| `nameSearch` | string | no | Search contacts by name. |
| `phoneSearch` | string | no | Search contacts by phone. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idSearch` | number | no | Search contacts by identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressSearch": "string",
      "digitalTrackingIdSearch": "string",
      "distributeLead": true,
      "emailSearch": "ava@example.com",
      "idSearch": 1,
      "limit": 1,
      "matches": [
        {}
      ],
      "message": "string",
      "nameSearch": "Ava Chen",
      "phoneSearch": "string",
      "resultCode": 1,
      "returnPmtOnFile": true,
      "skip": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressSearch` | string |  |
| `digitalTrackingIdSearch` | string |  |
| `distributeLead` | boolean |  |
| `emailSearch` | string |  |
| `idSearch` | number |  |
| `limit` | number |  |
| `matches` | array<object> |  |
| `message` | string |  |
| `nameSearch` | string |  |
| `phoneSearch` | string |  |
| `resultCode` | number |  |
| `returnPmtOnFile` | boolean |  |
| `skip` | number |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /contacts/locate` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

