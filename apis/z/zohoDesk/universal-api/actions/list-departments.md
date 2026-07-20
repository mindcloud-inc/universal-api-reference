# Zoho Desk: List Departments



```
GET https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-departments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Desk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoDesk/latest/actions/list-departments?${params}`, {
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
      "createdTime": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "description": "string",
      "id": "string",
      "isAssignToTeamEnabled": true,
      "isDefault": true,
      "isEnabled": true,
      "isVisibleInCustomerPortal": true,
      "name": "Ava Chen",
      "nameInCustomerPortal": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date |  |
| `creatorId` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isAssignToTeamEnabled` | boolean |  |
| `isDefault` | boolean |  |
| `isEnabled` | boolean |  |
| `isVisibleInCustomerPortal` | boolean |  |
| `name` | string |  |
| `nameInCustomerPortal` | string |  |

## Native endpoint

Through the native Zoho Desk API, this operation is `GET /departments` (base URL `https://desk.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-departments.md) for the provider-specific parameters and requirements.

