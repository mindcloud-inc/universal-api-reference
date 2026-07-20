# SMSINDIAHUB (India): Check Delivery Status



```
GET https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-delivery-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB (India) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-delivery-status?connectionId=$CONNECTION_ID&messageid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/check-delivery-status?${params}`, {
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
| `messageid` | string | yes | Provider job or message identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DoneDate": "string",
      "MobileNumber": "string",
      "Status": "string",
      "SubmitDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DoneDate` | string | Final delivery timestamp. |
| `MobileNumber` | string | Recipient mobile number. |
| `Status` | string | Delivery status. |
| `SubmitDate` | string | Submission timestamp. |

## Native endpoint

Through the native SMSINDIAHUB (India) API, this operation is `GET /vendorsms/checkdelivery.aspx` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-delivery-status.md) for the provider-specific parameters and requirements.

