# OnlineCheckWriter: Get Payee

Retrieves details for a specific payee.

```
GET https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-payee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnlineCheckWriter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-payee?connectionId=$CONNECTION_ID&payeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onlineCheckWriter/latest/actions/get-payee?${params}`, {
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
| `payeeId` | string | yes | The payee identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address1": "string",
        "address2": "string",
        "city": "string",
        "company": "string",
        "country": {},
        "dob": {},
        "email": {},
        "entityType": {},
        "id": "string",
        "name": "Ava Chen",
        "nickName": {},
        "phone": {},
        "state": "string",
        "zip": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.address1` | string |  |
| `data.address2` | string |  |
| `data.city` | string |  |
| `data.company` | string |  |
| `data.country` | object |  |
| `data.dob` | object |  |
| `data.email` | object |  |
| `data.entityType` | object |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.nickName` | object |  |
| `data.phone` | object |  |
| `data.state` | string |  |
| `data.zip` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native OnlineCheckWriter API, this operation is `GET /payees/:payeeId` (base URL `https://test.onlinecheckwriter.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payee.md) for the provider-specific parameters and requirements.

