# GorillaDesk: Retrieve Company

Retrieves company details from GorillaDesk.

```
GET https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GorillaDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gorillaDesk/latest/actions/retrieve-company?${params}`, {
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
      "address": "string",
      "city": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "officeHours": {
        "end": "string",
        "start": "string"
      },
      "phone": "string",
      "state": "string",
      "timezone": "string",
      "website": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `email` | string |  |
| `name` | string |  |
| `officeHours` | object |  |
| `officeHours.end` | string |  |
| `officeHours.start` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `timezone` | string |  |
| `website` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native GorillaDesk API, this operation is `GET /company` (base URL `https://api.gorilladesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-company.md) for the provider-specific parameters and requirements.

