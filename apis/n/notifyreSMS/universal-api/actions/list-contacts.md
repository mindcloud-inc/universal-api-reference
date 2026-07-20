# Notifyre SMS: List Contacts

Finds contacts in Notifyre by search filters.

```
GET https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/list-contacts?${params}`, {
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
| `groupIds` | list<string> | no | Restrict results to these groups. |
| `includeUnsubscribed` | boolean | no | Whether unsubscribed contacts should be included. |
| `limit` | number | no | Maximum contacts to return. |
| `page` | number | no | Page number for contacts listing. |
| `searchQuery` | string | no | Search term for contacts. |
| `sortBy` | string | no | Field used to sort contacts. |
| `sortDir` | string | no | Sort direction for contacts. |
| `type` | string | no | Contact type filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> | Contacts returned by the search request. |
| `totalCount` | number | Total matching contacts. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /addressbook/contacts/search` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

