# vionvi CRM: List Clients

Retrieves clients from vionvi CRM.

```
GET https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a vionvi CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vionviCRM/latest/actions/list-clients?${params}`, {
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
      "dob": "2026-05-07T12:00:00.000Z",
      "dtCreate": 1,
      "dtUpdate": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "isActive": 1,
      "patronymic": "string",
      "phone": 1,
      "surname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dob` | date |  |
| `dtCreate` | number |  |
| `dtUpdate` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `isActive` | number |  |
| `patronymic` | string |  |
| `phone` | number |  |
| `surname` | string |  |

## Native endpoint

Through the native vionvi CRM API, this operation is `GET /client` (base URL `https://280-crm-api.vionvi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

