# HR Partner: List Employee Contacts



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employee-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employee-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employee-contacts?${params}`, {
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
      "details": "string",
      "employee": {},
      "id": 1,
      "information": "string",
      "isEmergency": true,
      "isPrimary": true,
      "isPublic": true,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `information` | string |  |
| `isEmergency` | boolean |  |
| `isPrimary` | boolean |  |
| `isPublic` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /contacts` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-contacts.md) for the provider-specific parameters and requirements.

