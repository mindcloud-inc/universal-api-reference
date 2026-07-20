# Routee: Calculate the cost of a campaign carried out by a mailing list

Calculates the cost of a campaign carried out by a mailing list in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/calculate-the-cost-of-a-campaign-carried-out-by-a-mailing-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/calculate-the-cost-of-a-campaign-carried-out-by-a-mailing-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/calculate-the-cost-of-a-campaign-carried-out-by-a-mailing-list?${params}`, {
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
| `id` | string | yes | List ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressesDeltaFromBalance": 1,
      "addressesDeltaFromTariff": 1,
      "cur": "string",
      "max_emails_per_task": "ava@example.com",
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
| `max_emails_per_task` | string |  |
| `overdraftAllEmailsPrice` | number |  |
| `result` | boolean |  |
| `sent_emails_qty` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /addressbooks/:id/cost` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-the-cost-of-a-campaign-carried-out-by-a-mailing-list.md) for the provider-specific parameters and requirements.

