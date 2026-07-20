# PhantomBuster: Get Organization Resources

Retrieves organization resources from PhantomBuster.

```
GET https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/get-organization-resources?${params}`, {
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
      "agentCount": 1,
      "dailyAiCredit": 1,
      "dailyCaptcha": 1,
      "dailyDiscoveredMail": 1,
      "dailyExecutionTime": 1,
      "dailyMail": 1,
      "dailyResourceNextResetAt": 1,
      "dailySerpCredits": 1,
      "monthlyAiCredit": 1,
      "monthlyCaptcha": 1,
      "monthlyDiscoveredMail": 1,
      "monthlyExecutionTime": 1,
      "monthlyMail": 1,
      "monthlyResourceNextResetAt": 1,
      "monthlySerpCredits": 1,
      "plan": {
        "agents": 1,
        "dailyAiCredits": 1,
        "dailyCaptchas": 1,
        "dailyDiscoveredMails": 1,
        "dailyExecutionTime": 1,
        "dailyMails": 1,
        "dailySerpCredits": 1,
        "duration": 1,
        "isAvailable": true,
        "isUpgradable": true,
        "mongoStorage": 1,
        "monthlyAiCredits": 1,
        "monthlyCaptchas": 1,
        "monthlyDiscoveredMails": 1,
        "monthlyExecutionTime": 1,
        "monthlyPrice": 1,
        "monthlyPrices": {
          "eur": 1,
          "usd": 1
        },
        "monthlySerpCredits": 1,
        "name": "Ava Chen",
        "parallelism": 1,
        "s3Storage": 1,
        "scripts": 1,
        "yearlyPrice": 1,
        "yearlyPrices": {
          "eur": 1,
          "usd": 1
        }
      },
      "planName": "Ava Chen",
      "s3Storage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentCount` | number |  |
| `dailyAiCredit` | number |  |
| `dailyCaptcha` | number |  |
| `dailyDiscoveredMail` | number |  |
| `dailyExecutionTime` | number |  |
| `dailyMail` | number |  |
| `dailyResourceNextResetAt` | number |  |
| `dailySerpCredits` | number |  |
| `monthlyAiCredit` | number |  |
| `monthlyCaptcha` | number |  |
| `monthlyDiscoveredMail` | number |  |
| `monthlyExecutionTime` | number |  |
| `monthlyMail` | number |  |
| `monthlyResourceNextResetAt` | number |  |
| `monthlySerpCredits` | number |  |
| `plan.agents` | number |  |
| `plan.dailyAiCredits` | number |  |
| `plan.dailyCaptchas` | number |  |
| `plan.dailyDiscoveredMails` | number |  |
| `plan.dailyExecutionTime` | number |  |
| `plan.dailyMails` | number |  |
| `plan.dailySerpCredits` | number |  |
| `plan.duration` | number |  |
| `plan.isAvailable` | boolean |  |
| `plan.isUpgradable` | boolean |  |
| `plan.mongoStorage` | number |  |
| `plan.monthlyAiCredits` | number |  |
| `plan.monthlyCaptchas` | number |  |
| `plan.monthlyDiscoveredMails` | number |  |
| `plan.monthlyExecutionTime` | number |  |
| `plan.monthlyPrice` | number |  |
| `plan.monthlyPrices.eur` | number |  |
| `plan.monthlyPrices.usd` | number |  |
| `plan.monthlySerpCredits` | number |  |
| `plan.name` | string |  |
| `plan.parallelism` | number |  |
| `plan.s3Storage` | number |  |
| `plan.scripts` | number |  |
| `plan.yearlyPrice` | number |  |
| `plan.yearlyPrices.eur` | number |  |
| `plan.yearlyPrices.usd` | number |  |
| `planName` | string |  |
| `s3Storage` | number |  |

## Native endpoint

Through the native PhantomBuster API, this operation is `GET /orgs/fetch-resources` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-resources.md) for the provider-specific parameters and requirements.

