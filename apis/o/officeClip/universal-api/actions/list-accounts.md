# OfficeClip: List Accounts

Retrieves accounts from OfficeClip.

```
GET https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OfficeClip `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/officeClip/latest/actions/list-accounts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "accountName": "Ava Chen",
          "accountNumber": "string",
          "emailAddress": "ava@example.com",
          "id": "string",
          "mainPhone": "string",
          "security": {
            "append": true,
            "delete": true,
            "read": true,
            "write": true
          }
        }
      ],
      "pagination": {
        "first": "string",
        "last": "string",
        "next": "string",
        "prev": "string",
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].accountName` | string |  |
| `data[].accountNumber` | string |  |
| `data[].emailAddress` | string |  |
| `data[].id` | string |  |
| `data[].mainPhone` | string |  |
| `data[].security.append` | boolean |  |
| `data[].security.delete` | boolean |  |
| `data[].security.read` | boolean |  |
| `data[].security.write` | boolean |  |
| `pagination.first` | string |  |
| `pagination.last` | string |  |
| `pagination.next` | string |  |
| `pagination.prev` | string |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native OfficeClip API, this operation is `GET /api/account-summary` (base URL `https://app.officeclip.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

