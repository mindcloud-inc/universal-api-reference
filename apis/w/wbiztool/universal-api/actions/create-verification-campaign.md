# Wbiztool: Create Verification Campaign

Creates a WhatsApp number verification campaign in Wbiztool.

```
POST https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/create-verification-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/create-verification-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "numbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/create-verification-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "numbers[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `numbers[]` | array<string> | yes | Phone numbers to verify as an array. |
| `campaignName` | string | no | Optional label for the verification campaign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "message": "string",
      "numbersCount": 1,
      "numbersSubmitted": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `message` | string |  |
| `numbersCount` | number |  |
| `numbersSubmitted[]` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `POST /verification/create/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-verification-campaign.md) for the provider-specific parameters and requirements.

