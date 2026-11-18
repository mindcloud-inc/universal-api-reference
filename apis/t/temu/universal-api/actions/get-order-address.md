# Temu: Get Order Address

Retrieve shipping address information for a specific order.

```
GET https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order-address?connectionId=$CONNECTION_ID&parentOrderSn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parentOrderSn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temu/latest/actions/get-order-address?${params}`, {
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
| `parentOrderSn` | string | yes | The parent order serial number - 'parentOrderSn' |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLine1": "string",
      "addressLine2": "string",
      "addressLine3": {},
      "addressLineAll": "string",
      "backupMobile": {},
      "mail": "string",
      "mobile": "string",
      "postCode": "string",
      "receiptAdditionalName": {},
      "receiptName": "Ava Chen",
      "regionName1": "Ava Chen",
      "regionName2": "Ava Chen",
      "regionName3": "Ava Chen",
      "regionName4": {},
      "taxCode": {},
      "warning": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `addressLine3` | object |  |
| `addressLineAll` | string |  |
| `backupMobile` | object |  |
| `mail` | string |  |
| `mobile` | string |  |
| `postCode` | string |  |
| `receiptAdditionalName` | object |  |
| `receiptName` | string |  |
| `regionName1` | string |  |
| `regionName2` | string |  |
| `regionName3` | string |  |
| `regionName4` | object |  |
| `taxCode` | object |  |
| `warning` | object |  |

## Native endpoint

Through the native Temu API, this operation is `POST /router` (base URL `https://openapi-b-us.temu.com/openapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-address.md) for the provider-specific parameters and requirements.

