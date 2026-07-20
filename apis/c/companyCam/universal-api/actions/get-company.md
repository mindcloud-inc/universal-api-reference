# CompanyCam: Get Company

Retrieves the current company from CompanyCam.

```
GET https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyCam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyCam/latest/actions/get-company?${params}`, {
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
      "address": {
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string",
        "streetAddress1": "string",
        "streetAddress2": "string"
      },
      "id": 1,
      "logo": [
        {
          "type": "string",
          "uri": "string",
          "url": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.postalCode` | string |  |
| `address.state` | string |  |
| `address.streetAddress1` | string |  |
| `address.streetAddress2` | string |  |
| `id` | number |  |
| `logo[].type` | string |  |
| `logo[].uri` | string |  |
| `logo[].url` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native CompanyCam API, this operation is `GET company` (base URL `https://api.companycam.com/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

