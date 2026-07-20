# SendPulse: Get Mailing List Campaign Cost

Retrieves campaign cost for a SendPulse mailing list.

```
GET https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-mailing-list-campaign-cost
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendPulse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-mailing-list-campaign-cost?connectionId=$CONNECTION_ID&mailingListId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailingListId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendPulse/latest/actions/get-mailing-list-campaign-cost?${params}`, {
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
| `mailingListId` | string | yes | The SendPulse mailing list identifier. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressesDeltaFromBalance": 1,
      "addressesDeltaFromTariff": 1,
      "cur": "string",
      "max_emails_per_task": 1,
      "overdraftAllEmailsPrice": 1,
      "result": true,
      "sent_emails_qty": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressesDeltaFromBalance` | number |  |
| `addressesDeltaFromTariff` | number |  |
| `cur` | string |  |
| `max_emails_per_task` | number |  |
| `overdraftAllEmailsPrice` | number |  |
| `result` | boolean |  |
| `sent_emails_qty` | number |  |

## Native endpoint

Through the native SendPulse API, this operation is `GET /addressbooks/:mailingListId/cost` (base URL `https://api.sendpulse.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mailing-list-campaign-cost.md) for the provider-specific parameters and requirements.

