# Walmart: List Carrier Methods

Gets the available carrier methods

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-carrier-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-carrier-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-carrier-methods?${params}`, {
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
      "carrierMethodDisplayDescription": "string",
      "carrierMethodId": "string",
      "carrierMethodName": "Ava Chen",
      "carrierMethodType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierMethodDisplayDescription` | string |  |
| `carrierMethodId` | string |  |
| `carrierMethodName` | string |  |
| `carrierMethodType` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/carriers` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-carrier-methods.md) for the provider-specific parameters and requirements.

