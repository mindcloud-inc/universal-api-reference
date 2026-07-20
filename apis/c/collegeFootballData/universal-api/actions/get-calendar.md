# College Football Data: List Calendar

Retrieves season calendar information from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-calendar?connectionId=$CONNECTION_ID&year=2025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-calendar?${params}`, {
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
| `year` | number | yes | Required year filter Default: `2025`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "string",
      "firstGameStart": "string",
      "lastGameStart": "string",
      "season": 1,
      "seasonType": "string",
      "startDate": "string",
      "week": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | string |  |
| `firstGameStart` | string |  |
| `lastGameStart` | string |  |
| `season` | number |  |
| `seasonType` | string |  |
| `startDate` | string |  |
| `week` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /calendar` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar.md) for the provider-specific parameters and requirements.

