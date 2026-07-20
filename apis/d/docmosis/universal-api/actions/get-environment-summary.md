# Docmosis: Get Environment Summary



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-environment-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-environment-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-environment-summary?${params}`, {
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
      "accountEnvironmentSummary": {
        "accountEnvDetails": {
          "isActivated": true,
          "isDeleted": true,
          "isDisabled": true,
          "name": "Ava Chen"
        },
        "accountName": "Ava Chen",
        "pageQuota": {
          "isHardLimited": true,
          "pctUsed": 1,
          "pctUsedStr": "string",
          "quota": 1,
          "used": 1
        },
        "plan": {
          "name": "Ava Chen"
        },
        "ready": true
      },
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountEnvironmentSummary.accountEnvDetails.isActivated` | boolean |  |
| `accountEnvironmentSummary.accountEnvDetails.isDeleted` | boolean |  |
| `accountEnvironmentSummary.accountEnvDetails.isDisabled` | boolean |  |
| `accountEnvironmentSummary.accountEnvDetails.name` | string |  |
| `accountEnvironmentSummary.accountName` | string |  |
| `accountEnvironmentSummary.pageQuota.isHardLimited` | boolean |  |
| `accountEnvironmentSummary.pageQuota.pctUsed` | number |  |
| `accountEnvironmentSummary.pageQuota.pctUsedStr` | string |  |
| `accountEnvironmentSummary.pageQuota.quota` | number |  |
| `accountEnvironmentSummary.pageQuota.used` | number |  |
| `accountEnvironmentSummary.plan.name` | string |  |
| `accountEnvironmentSummary.ready` | boolean |  |
| `shortMsg` | string |  |
| `succeeded` | boolean |  |

## Native endpoint

Through the native Docmosis API, this operation is `POST /environment/summary` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment-summary.md) for the provider-specific parameters and requirements.

