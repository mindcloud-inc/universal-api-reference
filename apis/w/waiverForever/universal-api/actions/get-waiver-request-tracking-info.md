# WaiverForever: Get Waiver Request Tracking Info

Retrieves waiver request tracking info from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request-tracking-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request-tracking-info?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/get-waiver-request-tracking-info?${params}`, {
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
| `groupId` | string | yes | Waiver request group to inspect. |
| `page` | number | no | Results page number. |
| `perPage` | number | no | Results returned per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "page": 1,
      "perPage": 1,
      "trackings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of tracking records matching the query. |
| `page` | number | Current tracking results page. |
| `perPage` | number | Tracking records returned per page. |
| `trackings` | array<object> | Tracking rows for recipients in the waiver request group. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v2/waiverRequests/groupTrackings` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-waiver-request-tracking-info.md) for the provider-specific parameters and requirements.

