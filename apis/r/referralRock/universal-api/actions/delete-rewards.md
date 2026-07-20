# Referral Rock: Delete Rewards

Deletes existing rewards from Referral Rock.

```
DELETE https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-rewards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Referral Rock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-rewards?connectionId=$CONNECTION_ID&rewardIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rewardIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/delete-rewards?${params}`, {
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
| `rewardIds[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultInfo": {
        "message": {},
        "status": "string"
      },
      "rewardId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultInfo.message` | object |  |
| `resultInfo.status` | string |  |
| `rewardId` | string |  |

## Native endpoint

Through the native Referral Rock API, this operation is `POST /api/rewards/remove` (base URL `https://api.referralrock.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-rewards.md) for the provider-specific parameters and requirements.

