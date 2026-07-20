# Documo: List Contacts

Retrieves contact records from your Documo account.

```
GET https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documo/latest/actions/list-contacts?${params}`, {
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
| `userId` | string | no | User ID. If not specified, returns results for the current user. |
| `offset` | number | no | Number of results to skip for pagination. Default 0. |
| `limit` | number | no | Number of results to return. Default 50. |
| `order` | string | no | Sort order for results. Defaults to name asc. |
| `query` | string | no | Search by contact name, fax number, phone number, or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "query": {
        "limit": 1,
        "offset": 1,
        "query": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `query.limit` | number |  |
| `query.offset` | number |  |
| `query.query` | string |  |

## Native endpoint

Through the native Documo API, this operation is `GET /v1/contacts` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

