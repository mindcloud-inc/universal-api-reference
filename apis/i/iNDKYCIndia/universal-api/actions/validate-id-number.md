# IN-D KYC India: Validate ID Number

Retrieves ID number validation results from IN-D KYC India.

```
GET https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/validate-id-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/validate-id-number?connectionId=$CONNECTION_ID&docType=Aadhar%20Card%20Front&aadhar=123456789123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docType": "Aadhar Card Front",
  "aadhar": "123456789123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/validate-id-number?${params}`, {
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
| `docType` | string | yes | Document type to validate, for example Aadhar Card Front. Default: `Aadhar Card Front`. |
| `aadhar` | string | yes | Aadhaar number to validate. Default: `123456789123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "result": [
        {}
      ],
      "status": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string | Description returned by IN-D. |
| `result` | array<object> | Government database validation results. |
| `status` | string | Request status. |
| `uid` | string | UID assigned to the KYC process. |

## Native endpoint

Through the native IN-D KYC India API, this operation is `POST /api/validation/` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-id-number.md) for the provider-specific parameters and requirements.

