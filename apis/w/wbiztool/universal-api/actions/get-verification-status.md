# Wbiztool: Get Verification Status

Retrieves verification campaign status from Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-verification-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-verification-status?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/get-verification-status?${params}`, {
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
| `campaignId` | number | yes | Verification campaign ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "campaignName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "overallStatus": "string",
      "progress": {
        "completedPercentage": 1,
        "invalid": 1,
        "pending": 1,
        "total": 1,
        "verified": 1
      },
      "results": [
        {
          "checkedAt": "2026-05-07T12:00:00.000Z",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "number": "string",
          "status": "string"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `campaignName` | string |  |
| `createdAt` | date |  |
| `lastUpdated` | date |  |
| `overallStatus` | string |  |
| `progress.completedPercentage` | number |  |
| `progress.invalid` | number |  |
| `progress.pending` | number |  |
| `progress.total` | number |  |
| `progress.verified` | number |  |
| `results[].checkedAt` | date |  |
| `results[].createdAt` | date |  |
| `results[].number` | string |  |
| `results[].status` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `GET /verification/status/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-status.md) for the provider-specific parameters and requirements.

