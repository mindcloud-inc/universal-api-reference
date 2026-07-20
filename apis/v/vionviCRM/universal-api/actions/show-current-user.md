# vionvi CRM: Show Current User

Retrieves the current user from vionvi CRM.

```
GET https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/show-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vionvi CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/show-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/show-current-user?${params}`, {
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
      "dtDelete": 1,
      "email": "ava@example.com",
      "id": 1,
      "isActive": 1,
      "langLocale": "string",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dtDelete` | number |  |
| `email` | string |  |
| `id` | number |  |
| `isActive` | number |  |
| `langLocale` | string |  |
| `name` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native vionvi CRM API, this operation is `GET /user/show-me` (base URL `https://280-crm-api.vionvi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/show-current-user.md) for the provider-specific parameters and requirements.

