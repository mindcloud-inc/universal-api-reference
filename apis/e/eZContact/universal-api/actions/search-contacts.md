# EZContact: Search Contacts



```
GET https://connect.mindcloud.co/v1/universal/eZContact/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EZContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eZContact/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eZContact/latest/actions/search-contacts?${params}`, {
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
| `phoneNumber` | string | no | Partial phone number to search for. |
| `contactName` | string | no | Partial contact name to search for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resultLimit` | number | no | Maximum number of contacts to return. Default: `10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EZContact API returns.

## Native endpoint

Through the native EZContact API, this operation is `POST /mcp.php` (base URL `https://app.ezcontact.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

