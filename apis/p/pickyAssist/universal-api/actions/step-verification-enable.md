# Picky Assist: 2 Step Verification Enable



```
PUT https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/step-verification-enable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/step-verification-enable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pin": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/step-verification-enable', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pin": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pin` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /two-step-verification` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/step-verification-enable.md) for the provider-specific parameters and requirements.

