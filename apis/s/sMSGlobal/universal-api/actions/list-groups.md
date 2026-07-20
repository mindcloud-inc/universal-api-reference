# SMSGlobal: List Groups

Retrieves contact groups from the SMSGlobal account.

```
GET https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSGlobal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSGlobal/latest/actions/list-groups?${params}`, {
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
      "groups": [
        {
          "contactCount": 1,
          "defaultOrigin": "string",
          "id": 1,
          "isGlobal": true,
          "keyword": "string",
          "name": "Ava Chen"
        }
      ],
      "limit": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groups[].contactCount` | number | Number of contacts in the group. |
| `groups[].defaultOrigin` | string | Default SMS origin for the group. |
| `groups[].id` | number | Contact group identifier. |
| `groups[].isGlobal` | boolean | Whether the group is globally visible to sub accounts. |
| `groups[].keyword` | string | Email-to-SMS keyword for the group. |
| `groups[].name` | string | Group name. |
| `limit` | number | Number of group rows returned. |
| `offset` | number | Pagination offset. |
| `total` | number | Total number of contact groups. |

## Native endpoint

Through the native SMSGlobal API, this operation is `GET /v2/group` (base URL `https://api.smsglobal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

