# IdentityCheck: Generate KYB Report



```
POST https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/generate-kyb-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IdentityCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/generate-kyb-report" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "countryCode": "string",
  "registrationCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/identityCheck/latest/actions/generate-kyb-report', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "countryCode": "string",
    "registrationCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryCode` | string | yes | Company registration country code. |
| `registrationCode` | string | yes | Company registration code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "report": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.report` | string |  |

## Native endpoint

Through the native IdentityCheck API, this operation is `POST /v1/verification/namescan/kyb` (base URL `https://identity.stackgo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-kyb-report.md) for the provider-specific parameters and requirements.

