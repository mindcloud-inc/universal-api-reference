# Umami: Get Website Date Range



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-date-range?connectionId=$CONNECTION_ID&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-date-range?${params}`, {
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
| `websiteId` | string | yes | The website ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endDate": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endDate` | date | End of available data range. |
| `startDate` | date | Start of available data range. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/daterange` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-date-range.md) for the provider-specific parameters and requirements.

