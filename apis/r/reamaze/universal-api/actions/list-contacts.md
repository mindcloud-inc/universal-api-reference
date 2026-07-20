# Reamaze: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reamaze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reamaze/latest/actions/list-contacts?${params}`, {
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
| `q` | string | no | `q` with any string will search over contacts by name or email |
| `dataKeyValue` | string | no | `data` with a hash of key/value pairs (e.g. `data[key]=value`) will return contacts with `data` matching those key/value pairs. |
| `sort` | string | no | `sort` with value set to `date` will return results in descending order of create time. The default sort when this parameter is not provided is by name. |
| `date` | date | no | `sort` with value set to `date` will return results in descending order of create time. The default sort when this parameter is not provided is by name. |
| `type` | string | no | `type` with values set to `email` or `mobile` will return only contacts that have an email address or phone number, respectively. |
| `email` | string | no | `type` with values set to `email` or `mobile` will return only contacts that have an email address or phone number, respectively. |
| `mobile` | string | no | `type` with values set to `email` or `mobile` will return only contacts that have an email address or phone number, respectively. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {}
      ],
      "email": "ava@example.com",
      "friendlyName": "Ava Chen",
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "pageCount": 1,
      "pageSize": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | array<object> |  |
| `email` | string |  |
| `friendlyName` | string |  |
| `name` | string |  |
| `notes` | array<object> |  |
| `pageCount` | number |  |
| `pageSize` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Reamaze API, this operation is `GET /contacts` (base URL `https://{{credentials.brand}}.reamaze.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

