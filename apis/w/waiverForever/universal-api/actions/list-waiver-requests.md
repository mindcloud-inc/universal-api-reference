# WaiverForever: List Waiver Requests

Retrieves waiver requests from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-waiver-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-waiver-requests?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-waiver-requests?${params}`, {
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
| `endTimestamp` | number | no | End timestamp in seconds. |
| `includeWaivers` | boolean | no | Include submitted waivers in the response. |
| `name` | string | no | Optional name filter. |
| `page` | number | no | Results page number. |
| `perPage` | number | no | Results returned per page. |
| `requestIds` | list<string> | no | Specific waiver request ids to include. Accepts multiple values as an array. |
| `startTimestamp` | number | no | Start timestamp in seconds. |
| `status` | string | no | Optional status filter such as collecting or accepted. |
| `templateId` | string | yes | Template whose waiver requests should be listed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "page": 1,
      "perPage": 1,
      "waiverRequests": [
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
| `count` | number | Total number of matching waiver requests. |
| `page` | number | Current page number. |
| `perPage` | number | Page size. |
| `waiverRequests` | array<object> | Waiver request records. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v2/waiverRequests` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-waiver-requests.md) for the provider-specific parameters and requirements.

