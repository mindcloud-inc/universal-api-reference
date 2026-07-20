# Referral Rock: List Reward Rules

Retrieves member reward rules from Referral Rock.

```
GET https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-reward-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-reward-rules?connectionId=$CONNECTION_ID&programId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "programId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-reward-rules?${params}`, {
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
| `programId` | string | yes | ID of the program. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryDelay": 1,
      "deliveryType": "string",
      "description": "string",
      "isEnabled": true,
      "payoutDescription": "string",
      "payoutId": "string",
      "payoutType": "string",
      "programId": "string",
      "reward": {},
      "ruleEndDate": "2026-05-07T12:00:00.000Z",
      "ruleId": "string",
      "ruleStartDate": "2026-05-07T12:00:00.000Z",
      "trigger": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryDelay` | number |  |
| `deliveryType` | string |  |
| `description` | string |  |
| `isEnabled` | boolean |  |
| `payoutDescription` | string |  |
| `payoutId` | string |  |
| `payoutType` | string |  |
| `programId` | string |  |
| `reward` | object |  |
| `ruleEndDate` | date |  |
| `ruleId` | string |  |
| `ruleStartDate` | date |  |
| `trigger` | object |  |

## Native endpoint

Through the native Referral Rock API, this operation is `GET /api/rewardrules` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reward-rules.md) for the provider-specific parameters and requirements.

