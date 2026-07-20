# KYVE: Get Team Info



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-team-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-team-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-team-info?${params}`, {
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
      "available_account_rewards": "string",
      "available_authority_rewards": "string",
      "available_team_allocation": "string",
      "bcp_authority": "string",
      "claimed_account_rewards": "string",
      "claimed_authority_rewards": "string",
      "foundation_authority": "string",
      "issued_team_allocation": "string",
      "required_module_balance": "string",
      "team_module_balance": "string",
      "total_account_rewards": "string",
      "total_authority_rewards": "string",
      "total_team_allocation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available_account_rewards` | string |  |
| `available_authority_rewards` | string |  |
| `available_team_allocation` | string |  |
| `bcp_authority` | string |  |
| `claimed_account_rewards` | string |  |
| `claimed_authority_rewards` | string |  |
| `foundation_authority` | string |  |
| `issued_team_allocation` | string |  |
| `required_module_balance` | string |  |
| `team_module_balance` | string |  |
| `total_account_rewards` | string |  |
| `total_authority_rewards` | string |  |
| `total_team_allocation` | string |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/team/v1beta1/team_info` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-info.md) for the provider-specific parameters and requirements.

