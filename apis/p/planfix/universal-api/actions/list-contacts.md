# Planfix: List Contacts

Retrieves contacts and companies from Planfix.

```
GET https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planfix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-contacts?${params}`, {
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
| `fields` | string | no | Comma-delimited contact fields to return. Default: `id,name,isCompany,email`. |
| `pageSize` | number | no | Number of contacts to return. Default: `100`. |
| `offset` | number | no | Contact list offset. Default: `0`. |
| `isCompany` | boolean | no | True for companies, false for people. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterId` | string | no | Saved Planfix contact filter identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "isCompany": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | number |  |
| `isCompany` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Planfix API, this operation is `POST /contact/list` (base URL `{{credentials.accountBaseUrl}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

