# EasyBroker: Retrieve Location

Retrieves location details from EasyBroker.

```
GET https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/retrieve-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyBroker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/retrieve-location?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyBroker/latest/actions/retrieve-location?${params}`, {
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
      "fullName": "Ava Chen",
      "localities": [
        {
          "fullName": "Ava Chen",
          "name": "Ava Chen",
          "type": "string"
        }
      ],
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullName` | string |  |
| `localities[].fullName` | string |  |
| `localities[].name` | string |  |
| `localities[].type` | string |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native EasyBroker API, this operation is `GET /locations` (base URL `https://api.easybroker.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-location.md) for the provider-specific parameters and requirements.

