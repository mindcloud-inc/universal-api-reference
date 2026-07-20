# Wbiztool: List Verification Results

Retrieves verification results for a campaign in Wbiztool.

```
GET https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-verification-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wbiztool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-verification-results?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wbiztool/latest/actions/list-verification-results?${params}`, {
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
| `campaignId` | number | yes | Verification campaign ID to list results for. |
| `status` | string | no | Optional result status filter. |
| `limit` | number | no | Maximum number of results to return. |
| `offset` | string | no | Result offset for pagination. Pass numeric text such as 0, 25, or 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "campaignName": "Ava Chen",
      "checkedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "number": "string",
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
| `checkedAt` | date |  |
| `createdAt` | date |  |
| `id` | number |  |
| `number` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Wbiztool API, this operation is `GET /verification/results/` (base URL `https://wbiztool.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-verification-results.md) for the provider-specific parameters and requirements.

