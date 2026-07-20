# Eagle Doc: Get Monthly Usage History

Retrieves monthly usage history from Eagle Doc.

```
GET https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-monthly-usage-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-monthly-usage-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-monthly-usage-history?${params}`, {
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
      "additionalInfo": {
        "contractQuota": 1,
        "pricePerPage": 1,
        "pricePerPageOverUsage": 1
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "quotaDate": "string",
      "quotaEndTime": "2026-05-07T12:00:00.000Z",
      "quotaPaymentMethod": "string",
      "quotaStartTime": "2026-05-07T12:00:00.000Z",
      "quotaUsed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo.contractQuota` | number |  |
| `additionalInfo.pricePerPage` | number |  |
| `additionalInfo.pricePerPageOverUsage` | number |  |
| `createdAt` | date |  |
| `quotaDate` | string |  |
| `quotaEndTime` | date |  |
| `quotaPaymentMethod` | string |  |
| `quotaStartTime` | date |  |
| `quotaUsed` | number |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `GET /api/usage/v1/monthly` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monthly-usage-history.md) for the provider-specific parameters and requirements.

