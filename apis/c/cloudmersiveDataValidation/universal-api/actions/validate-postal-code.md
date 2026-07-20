# Cloudmersive Data Validation: Validate Postal Code

Validates a postal code with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-postal-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-postal-code?connectionId=$CONNECTION_ID&input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-postal-code?${params}`, {
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
| `input` | object | yes | Postal code validation request object containing postal code and country details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "City": "string",
      "Latitude": 1,
      "Longitude": 1,
      "StateOrProvince": "string",
      "ValidPostalCode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `City` | string |  |
| `Latitude` | number |  |
| `Longitude` | number |  |
| `StateOrProvince` | string |  |
| `ValidPostalCode` | boolean |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/address/postal-code` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-postal-code.md) for the provider-specific parameters and requirements.

