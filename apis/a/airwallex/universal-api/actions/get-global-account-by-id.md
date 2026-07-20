# Airwallex: Get Global Account by ID

Retrieves a global account by ID from Airwallex.

```
GET https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-global-account-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-global-account-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-global-account-by-id?${params}`, {
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
| `globalAccountId` | string | no | The Airwallex global account ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountName": "Ava Chen",
      "accountNumber": "string",
      "accountType": "string",
      "countryCode": "string",
      "id": "string",
      "institution": {
        "address": "string",
        "city": "string",
        "name": "Ava Chen",
        "zipCode": "string"
      },
      "nickName": "Ava Chen",
      "requestId": "string",
      "requiredFeatures": [
        {
          "currency": "string",
          "transferMethod": "string"
        }
      ],
      "status": "string",
      "supportedFeatures": [
        {
          "currency": "string",
          "localClearingSystem": "string",
          "routingCodes": [
            {
              "type": "string",
              "value": "string"
            }
          ],
          "transferMethod": "string",
          "type": "string"
        }
      ],
      "swiftCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountName` | string |  |
| `accountNumber` | string |  |
| `accountType` | string |  |
| `countryCode` | string |  |
| `id` | string |  |
| `institution.address` | string |  |
| `institution.city` | string |  |
| `institution.name` | string |  |
| `institution.zipCode` | string |  |
| `nickName` | string |  |
| `requestId` | string |  |
| `requiredFeatures[].currency` | string |  |
| `requiredFeatures[].transferMethod` | string |  |
| `status` | string |  |
| `supportedFeatures[].currency` | string |  |
| `supportedFeatures[].localClearingSystem` | string |  |
| `supportedFeatures[].routingCodes[].type` | string |  |
| `supportedFeatures[].routingCodes[].value` | string |  |
| `supportedFeatures[].transferMethod` | string |  |
| `supportedFeatures[].type` | string |  |
| `swiftCode` | string |  |

## Native endpoint

Through the native Airwallex API, this operation is `GET /api/v1/global_accounts/{{globalAccountId}}` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-global-account-by-id.md) for the provider-specific parameters and requirements.

