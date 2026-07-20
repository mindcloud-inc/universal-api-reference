# Amazon Seller: Get Order Regulated Info

Retrieves regulated information for an Amazon Seller order.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-regulated-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-regulated-info?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-regulated-info?${params}`, {
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
| `orderId` | string | yes | The Amazon order identifier in 3-7-7 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amazonOrderId": "string",
      "regulatedInformation": {
        "fields": [
          {
            "fieldId": "string",
            "fieldLabel": "string",
            "fieldType": "string",
            "fieldValue": "string"
          }
        ]
      },
      "regulatedOrderVerificationStatus": {
        "externalReviewerId": "string",
        "rejectionReason": {
          "rejectionReasonDescription": "string",
          "rejectionReasonId": "string"
        },
        "requiresMerchantAction": true,
        "reviewDate": "string",
        "status": "string",
        "validRejectionReasons": [
          {
            "rejectionReasonDescription": "string",
            "rejectionReasonId": "string"
          }
        ],
        "validVerificationDetails": [
          {
            "validVerificationStatuses": [
              "string"
            ],
            "verificationDetailType": "string"
          }
        ]
      },
      "requiresDosageLabel": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amazonOrderId` | string |  |
| `regulatedInformation.fields[].fieldId` | string |  |
| `regulatedInformation.fields[].fieldLabel` | string |  |
| `regulatedInformation.fields[].fieldType` | string |  |
| `regulatedInformation.fields[].fieldValue` | string |  |
| `regulatedOrderVerificationStatus.externalReviewerId` | string |  |
| `regulatedOrderVerificationStatus.rejectionReason.rejectionReasonDescription` | string |  |
| `regulatedOrderVerificationStatus.rejectionReason.rejectionReasonId` | string |  |
| `regulatedOrderVerificationStatus.requiresMerchantAction` | boolean |  |
| `regulatedOrderVerificationStatus.reviewDate` | string |  |
| `regulatedOrderVerificationStatus.status` | string |  |
| `regulatedOrderVerificationStatus.validRejectionReasons[].rejectionReasonDescription` | string |  |
| `regulatedOrderVerificationStatus.validRejectionReasons[].rejectionReasonId` | string |  |
| `regulatedOrderVerificationStatus.validVerificationDetails[].validVerificationStatuses[]` | string |  |
| `regulatedOrderVerificationStatus.validVerificationDetails[].verificationDetailType` | string |  |
| `requiresDosageLabel` | boolean |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET orders/v0/orders/:orderId/regulatedInfo` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-regulated-info.md) for the provider-specific parameters and requirements.

