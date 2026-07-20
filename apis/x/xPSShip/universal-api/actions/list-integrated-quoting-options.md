# XPS Ship: List Integrated Quoting Options

Retrieves integrated quoting options from XPS Ship.

```
GET https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-integrated-quoting-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XPS Ship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-integrated-quoting-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xPSShip/latest/actions/list-integrated-quoting-options?${params}`, {
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
      "carrierCode": "string",
      "integratedQuotingOptions": [
        {}
      ],
      "name": "Ava Chen",
      "packageTypeCode": "string",
      "serviceCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrierCode` | string |  |
| `integratedQuotingOptions` | array<object> |  |
| `name` | string |  |
| `packageTypeCode` | string |  |
| `serviceCode` | string |  |

## Native endpoint

Through the native XPS Ship API, this operation is `GET /restapi/v1/customers/:customerId/integratedQuotingOptions` (base URL `https://xpsshipper.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-integrated-quoting-options.md) for the provider-specific parameters and requirements.

