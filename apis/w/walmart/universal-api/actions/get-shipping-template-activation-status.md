# Walmart: Get Shipping Template Activation Status

Get the Activation Status of the Shipping Templates, which are set through Walmart Seller Center.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-template-activation-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-template-activation-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-shipping-template-activation-status?${params}`, {
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
      "activationStatus": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "modifiedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activationStatus` | string |  |
| `createdDate` | date |  |
| `modifiedDate` | date |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/settings/shipping/templates/activationStatus` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipping-template-activation-status.md) for the provider-specific parameters and requirements.

