# Harness: List Users

Retrieves users from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-users?${params}`, {
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
| `emails` | list<string> | no | Filter by user emails. |
| `identifiers` | list<string> | no | Filter by user identifiers. |
| `parentFilter` | string | no | Parent-scope filter mode. |
| `searchTerm` | string | no | Search users by name or email. |
| `sortOrders` | string | no | Serialized sort order payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "empty": true,
      "pageIndex": 1,
      "pageItemCount": 1,
      "pageSize": 1,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `empty` | boolean | Whether the page has no users. |
| `pageIndex` | number | Zero-based page index. |
| `pageItemCount` | number | Users returned in this page. |
| `pageSize` | number | Requested page size. |
| `totalItems` | number | Total number of users. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Harness API, this operation is `POST /ng/api/user/batch` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

