# Wati: List Contacts

Retrieves contacts from Wati using optional filters.

```
GET https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wati `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wati/latest/actions/list-contacts?${params}`, {
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
| `pageSize` | number | no | Number of contacts to return per page. Default: `10`. |
| `pageNumber` | number | no | Page number to return. Default: `1`. |
| `name` | string | no | Filter contacts by name. |
| `attribute` | string | no | Filter contacts by attribute. |
| `createdDate` | date | no | Filter contacts by created date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loginUserPhone": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loginUserPhone` | string | Connected Wati phone number returned by the tenant. |
| `result` | string | Provider status string. |

## Native endpoint

Through the native Wati API, this operation is `GET /api/v1/getContacts` (base URL `{{credentials.apiEndpointUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

