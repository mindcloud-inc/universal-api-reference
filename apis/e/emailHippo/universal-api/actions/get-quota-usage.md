# Email Hippo: Get Quota Usage

Retrieves quota usage details from Email Hippo.

```
GET https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/get-quota-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Email Hippo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/get-quota-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/get-quota-usage?${params}`, {
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
      "accountId": 1,
      "errorSummary": "string",
      "licenseKey": "string",
      "nextQuotaResetDate": "string",
      "quotaRemaining": 1,
      "quotaUsed": 1,
      "reportedDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `errorSummary` | string |  |
| `licenseKey` | string |  |
| `nextQuotaResetDate` | string |  |
| `quotaRemaining` | number |  |
| `quotaUsed` | number |  |
| `reportedDate` | string |  |

## Native endpoint

Through the native Email Hippo API, this operation is `GET customer/reports/v3/quota/{{credentials.apiKey}}` (base URL `https://api.hippoapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quota-usage.md) for the provider-specific parameters and requirements.

