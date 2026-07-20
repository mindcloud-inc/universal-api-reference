# MojoTxt: Update Donation Keyword

Updates a donation keyword in MojoTxt.

```
PUT https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-donation-keyword
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-donation-keyword" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "donationIdOrKeyword": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-donation-keyword', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "donationIdOrKeyword": "string",
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
| `donationIdOrKeyword` | string | yes | The donation keyword identifier or keyword value to update. |
| `fundName` | string | no | The updated fund name for the donation keyword. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `recurringScheduleId` | number | no | Default recurring schedule: 0 one-time, 1 weekly, 2 bi-weekly, 3 monthly, or empty to ask the user. |
| `thankYou` | string | no | Thank-you message sent after a successful donation. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `message` | string | Human-readable update result message. |
| `result` | string | Whether the update request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `POST /:phoneNumber/donations/update/:donationIdOrKeyword` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-donation-keyword.md) for the provider-specific parameters and requirements.

