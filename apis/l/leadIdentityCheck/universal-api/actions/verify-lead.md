# Lead Identity Check: Verify Lead



```
GET https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/verify-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lead Identity Check `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/verify-lead?connectionId=$CONNECTION_ID&firstname=Ava&lastname=Chen&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstname": "Ava",
  "lastname": "Chen",
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/verify-lead?${params}`, {
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
| `firstname` | string | yes | Lead first name. |
| `lastname` | string | yes | Lead last name. |
| `phone` | string | yes | Lead phone number. |
| `email` | string | no | Lead email address. |
| `address` | object | no | Optional object with Street, City, State, and Zipcode keys. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Address": {},
      "Email": {},
      "Master Response": "string",
      "Phone": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Address` | object | Address verification results returned by the selected filter. |
| `Email` | object | Email verification results returned by the selected filter. |
| `Master Response` | string | Overall pass or fail result for the lead check. |
| `Phone` | object | Phone verification results returned by the selected filter. |

## Native endpoint

Through the native Lead Identity Check API, this operation is `POST /main/lic/v1` (base URL `https://leadidentitycheck-node.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-lead.md) for the provider-specific parameters and requirements.

