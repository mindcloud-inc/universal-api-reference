# Referral Rock: List Payouts

Retrieves payout records from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-payouts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "payoutPrograms": [
        {}
      ],
      "payoutType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `payoutPrograms` | array<object> |  |
| `payoutType` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/payouts` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payouts.md) for the provider-specific parameters and requirements.

