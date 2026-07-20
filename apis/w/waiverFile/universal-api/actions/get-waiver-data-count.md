# WaiverFile: Get Waiver Data Count

Retrieves waiver data count from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-waiver-data-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-waiver-data-count?connectionId=$CONNECTION_ID&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-waiver-data-count?${params}`, {
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
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetWaiverDataCount` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-waiver-data-count.md) for the provider-specific parameters and requirements.

