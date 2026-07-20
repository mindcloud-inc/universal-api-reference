# Eagle Doc: Get Quota Summary

Retrieves quota summary from Eagle Doc.

```
GET https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-quota-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-quota-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/get-quota-summary?${params}`, {
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
      "currentMonth": "string",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "quota": 1,
      "quotaUsed": 1,
      "startedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentMonth` | string | Current billing month in YYYY-MM format |
| `endedAt` | date | Billing period end time |
| `quota` | number | Pages included in the current contract period |
| `quotaUsed` | number | Pages processed in the current contract period |
| `startedAt` | date | Billing period start time |

## Native endpoint

Through the native Eagle Doc API, this operation is `GET /api/management/v1/quota` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-quota-summary.md) for the provider-specific parameters and requirements.

