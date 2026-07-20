# Retently: Get Group Trends

Retrieves trend data for a group from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-group-trends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-group-trends?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-group-trends?${params}`, {
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
| `groupId` | string | yes | Group Id |
| `date` | string | no | Date range preset supporting the following ptions: today, yesterday, past-week, past-month, past-3-months, past-6-months, past-year, this-month-to-date, this-quarter-to-date, this-year-to-date, custom. |
| `startDate` | string | no | Custom start date in ISO format or UNIX timestamp. |
| `endDate` | string | no | Custom end date in ISO format or UNIX timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateRange": {},
      "group": {},
      "success": true,
      "trends": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateRange` | object |  |
| `group` | object |  |
| `success` | boolean |  |
| `trends` | array<string> |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/trends/:groupId` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group-trends.md) for the provider-specific parameters and requirements.

