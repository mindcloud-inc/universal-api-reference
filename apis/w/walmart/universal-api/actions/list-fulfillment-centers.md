# Walmart: List Fulfillment Centers

Provides a list of all the fulfillment centers

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-fulfillment-centers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-fulfillment-centers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/list-fulfillment-centers?${params}`, {
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
| `includeCalendarDayConfiguration` | boolean | no | Flag to specify if calendarDayConfiguration block will be included in the response. Allowed values are true or false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customNodeId": "string",
      "distributorSupportedServices": [
        "string"
      ],
      "nodeType": "string",
      "postalAddress": {
        "addressLine1": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "shipNode": "string",
      "shipNodeName": "Ava Chen",
      "shippingDetails": [
        {
          "twoDayShipping": [
            {
              "carrierMethodName": "Ava Chen",
              "carrierMethodType": "string"
            }
          ]
        }
      ],
      "status": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customNodeId` | string |  |
| `distributorSupportedServices[]` | string |  |
| `nodeType` | string |  |
| `postalAddress.addressLine1` | string |  |
| `postalAddress.city` | string |  |
| `postalAddress.country` | string |  |
| `postalAddress.postalCode` | string |  |
| `postalAddress.state` | string |  |
| `shipNode` | string |  |
| `shipNodeName` | string |  |
| `shippingDetails[].twoDayShipping[].carrierMethodName` | string |  |
| `shippingDetails[].twoDayShipping[].carrierMethodType` | string |  |
| `status` | string |  |
| `timeZone` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/shipnodes` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fulfillment-centers.md) for the provider-specific parameters and requirements.

