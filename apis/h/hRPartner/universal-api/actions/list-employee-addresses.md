# HR Partner: List Employee Addresses



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employee-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employee-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/list-employee-addresses?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "country": "string",
      "employee": {},
      "id": 1,
      "postCode": "string",
      "state": "string",
      "suburb": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address1` | string |  |
| `address2` | string |  |
| `country` | string |  |
| `employee` | object |  |
| `id` | number |  |
| `postCode` | string |  |
| `state` | string |  |
| `suburb` | string |  |
| `type` | string |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /addresses` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-addresses.md) for the provider-specific parameters and requirements.

