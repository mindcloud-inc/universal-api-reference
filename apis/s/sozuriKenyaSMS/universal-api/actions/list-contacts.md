# Sozuri (Kenya) SMS: List Contacts

Retrieves contacts from Sozuri.

```
GET https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sozuri (Kenya) SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sozuriKenyaSMS/latest/actions/list-contacts?${params}`, {
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
| `group` | string | no | The group name to fetch contacts from. If omitted, all contacts are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": {},
      "group": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts` | object |  |
| `group` | string |  |

## Native endpoint

Through the native Sozuri (Kenya) SMS API, this operation is `GET /contacts` (base URL `https://sozuri.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

