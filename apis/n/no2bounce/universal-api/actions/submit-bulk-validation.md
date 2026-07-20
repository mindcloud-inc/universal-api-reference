# no2bounce: Submit Bulk Validation

Creates a bulk validation job in no2bounce.

```
POST https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/submit-bulk-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a no2bounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/submit-bulk-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailList[]": "Add one or more email addresses"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/no2bounce/latest/actions/submit-bulk-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailList[]": "Add one or more email addresses"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailList[]` | array<string> | yes | Provide one or more email addresses to validate. Example: `Add one or more email addresses`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "trackingId": "string"
      },
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.trackingId` | string |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native no2bounce API, this operation is `POST /n2b_validate_bulk` (base URL `https://connect.no2bounce.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-bulk-validation.md) for the provider-specific parameters and requirements.

