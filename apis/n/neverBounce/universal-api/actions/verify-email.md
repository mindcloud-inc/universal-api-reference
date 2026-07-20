# NeverBounce: Verify Email

Verifies an email address in NeverBounce.

```
GET https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeverBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neverBounce/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | Email address to verify. |
| `addressInfo` | boolean | no | Include parsed address details in the verification response. |
| `creditsInfo` | boolean | no | Include credit usage details in the verification response. |
| `timeout` | number | no | Maximum verification time before returning an unknown result. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "executionTime": 1,
      "flags": [
        "string"
      ],
      "result": "string",
      "status": "string",
      "suggestedCorrection": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `executionTime` | number |  |
| `flags` | array<string> |  |
| `result` | string |  |
| `status` | string |  |
| `suggestedCorrection` | string |  |

## Native endpoint

Through the native NeverBounce API, this operation is `GET /single/check` (base URL `https://api.neverbounce.com/v4.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

