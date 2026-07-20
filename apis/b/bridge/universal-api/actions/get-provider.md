# Bridge: Get Provider

Retrieves a provider from Bridge.

```
GET https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-provider
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-provider?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridge/latest/actions/get-provider?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregationMetadata": {
        "releaseStatus": "string"
      },
      "capabilities": [
        "string"
      ],
      "countryCode": "string",
      "groupName": "Ava Chen",
      "healthStatus": {},
      "id": 1,
      "images": {
        "logo": "string"
      },
      "name": "Ava Chen",
      "paymentMetadata": {
        "executionStatusAvailable": true,
        "maxSizeLabel": 1,
        "nbMaxTransactions": 1,
        "providerEnvironments": [
          "string"
        ],
        "releaseStatus": "string",
        "senderIbanAvailable": true
      },
      "tags": {
        "keywords": [
          "string"
        ],
        "region": [
          "string"
        ],
        "segment": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregationMetadata` | object | Properties and available features relative to the aggregation and account capabilities |
| `aggregationMetadata.releaseStatus` | string | Deployment state of the providers' aggregation capabilities |
| `capabilities` | array<string> | An array of the provider capabilities |
| `countryCode` | string | Provider's ISO 3166-1 alpha-2 country code |
| `groupName` | string | If the provider can be grouped, then we will expose its group name here |
| `healthStatus` | object | Provider's health status by capability |
| `id` | number | Provider's unique identifier |
| `images` | object | List of provider images, primarily logos |
| `images.logo` | string | Provider's logo |
| `name` | string | Provider's name |
| `paymentMetadata` | object | Properties and available features relative to all the payment capabilities |
| `paymentMetadata.executionStatusAvailable` | boolean | Indicates if the provider can provide execution status for payments |
| `paymentMetadata.maxSizeLabel` | number | The maximum length of the transaction label, in characters |
| `paymentMetadata.nbMaxTransactions` | number | The maximum number of transactions allowed per payment |
| `paymentMetadata.providerEnvironments` | array<string> | Supported Bridge environments for using payment with this provider |
| `paymentMetadata.releaseStatus` | string | Deployment state of the providers' payment capabilities |
| `paymentMetadata.senderIbanAvailable` | boolean | Indicates whether the sender's IBAN information (IBAN of the payer's account) is available |
| `tags` | object | Complementary metadata about the institution abstracted by the provider |
| `tags.keywords` | array<string> | Array of strings associated to the provider's name |
| `tags.region` | array<string> | Indicates the geographical areas where the provider operates |
| `tags.segment` | array<string> | Specifies the target market of the provider with possible values being `b2c` for individual consumers and `b2b` for businesses |

## Native endpoint

Through the native Bridge API, this operation is `GET /providers/:id` (base URL `https://api.bridgeapi.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-provider.md) for the provider-specific parameters and requirements.

