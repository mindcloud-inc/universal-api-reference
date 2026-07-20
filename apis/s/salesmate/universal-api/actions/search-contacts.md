# Salesmate: Search Contacts



```
GET https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/search-contacts?${params}`, {
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
| `filterQuery` | object | no | Salesmate search filter object. Default: `{"group":{"rules":[{"data":"Jan 01, 1970 05:30 AM","field":{"type":"DateTime","fieldName":"contact.createdAt","displayName":"Created At"},"condition":"IS_AFTER","eventType":"DateTime","moduleName":"Contact"}],"operator":"AND"}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "owner": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Primary email address. |
| `id` | number | Contact ID. |
| `name` | string | Contact display name. |
| `owner` | number | Owner user ID. |

## Native endpoint

Through the native Salesmate API, this operation is `POST /contact/v4/search` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

