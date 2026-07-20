# IN-D KYC India: Validate ID Number For UID

Retrieves ID number validation results in IN-D KYC India by UID.

```
GET https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/validate-id-number-for-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IN-D KYC India `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/validate-id-number-for-uid?connectionId=$CONNECTION_ID&uid=test-uid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "test-uid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNDKYCIndia/latest/actions/validate-id-number-for-uid?${params}`, {
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
| `uid` | string | yes | UID returned by Generate UID. Default: `test-uid`. |

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

Through the native IN-D KYC India API, this operation is `POST /api/validation/{uid}` (base URL `https://api.kyc.in-d.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-id-number-for-uid.md) for the provider-specific parameters and requirements.

