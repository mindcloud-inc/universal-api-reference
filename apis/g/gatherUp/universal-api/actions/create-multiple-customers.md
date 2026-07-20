# GatherUp: Create Multiple Customers

Creates multiple new customers in GatherUp.

```
POST https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-multiple-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-multiple-customers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": 1,
  "customerEmail{N}": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-multiple-customers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": 1,
    "customerEmail{N}": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | number | yes | Business id. |
| `customerCustomId{N}` | string | no | Customer custom id. |
| `customerEmail{N}` | string | yes | Customer email address. This field is required for basic plan accounts. For higher plans there is email or phone number required. |
| `customerFirstName{N}` | string | no | Customer first name. |
| `customerJobId{N}` | string | no | Customer job id. |
| `customerLastName{N}` | string | no | Customer last name. |
| `customerPhone{N}` | string | no | Customer phone. |
| `customerPreference{N}` | string | no | Customer communication preference. |
| `customerTags{N}` | string | no | Customer tags separated by comma (max length of one tag = 50 chars). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerErrorCode": 1,
      "customerErrorMessage": "string",
      "customerId": 1,
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerErrorCode` | number |  |
| `customerErrorMessage` | string |  |
| `customerId` | number |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /customers/create` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-multiple-customers.md) for the provider-specific parameters and requirements.

