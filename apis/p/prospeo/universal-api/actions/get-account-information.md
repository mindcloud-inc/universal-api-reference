# Prospeo: Get Account Information

Retrieves account information from Prospeo.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/get-account-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/get-account-information?${params}`, {
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
      "currentPlan": "string",
      "currentTeamMembers": 1,
      "nextQuotaRenewalDate": "string",
      "nextQuotaRenewalDays": 1,
      "remainingCredits": 1,
      "usedCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPlan` | string |  |
| `currentTeamMembers` | number |  |
| `nextQuotaRenewalDate` | string |  |
| `nextQuotaRenewalDays` | number |  |
| `remainingCredits` | number |  |
| `usedCredits` | number |  |

## Native endpoint

Through the native Prospeo API, this operation is `GET /account-information` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-information.md) for the provider-specific parameters and requirements.

