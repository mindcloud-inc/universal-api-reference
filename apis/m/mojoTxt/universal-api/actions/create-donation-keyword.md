# MojoTxt: Create Donation Keyword

Creates a donation keyword in MojoTxt.

```
POST https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-donation-keyword
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-donation-keyword" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyword": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-donation-keyword', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyword": "string",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amountRequestMessage` | string | no | Prompt sent when no donation amount is supplied. |
| `ccbFund` | number | no | Church Community Builder fund number for exports. |
| `defaultAmount` | number | no | Default donation amount if the donor does not specify one. |
| `fundName` | string | no | Fund name for the donation keyword. MojoTxt currently defaults this when omitted, despite the docs marking it required. |
| `keyword` | string | yes | The unique keyword for the donation fund. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `recurringScheduleId` | number | no | Default recurring schedule: 0 one-time, 1 weekly, 2 bi-weekly, 3 monthly, or empty to ask the user. |
| `thankYou` | string | no | Thank-you message sent after a successful donation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_id": 1,
      "message": "string",
      "result": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_id` | number | ID of the newly created donation keyword. |
| `message` | string | Human-readable create result message. |
| `result` | string | Whether the create request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `POST /:phoneNumber/donations/add` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-donation-keyword.md) for the provider-specific parameters and requirements.

