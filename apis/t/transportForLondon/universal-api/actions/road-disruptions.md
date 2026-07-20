# Transport for London: Get Road Disruptions

Retrieves road disruptions for selected roads in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/road-disruptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/road-disruptions?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/road-disruptions?${params}`, {
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
| `ids` | string | yes | Comma-separated TfL road IDs, such as A1,A2. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "comments": "string",
      "corridorIds": [
        "string"
      ],
      "currentUpdate": "string",
      "currentUpdateDateTime": "2026-05-07T12:00:00.000Z",
      "endDateTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "location": "string",
      "severity": "string",
      "startDateTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "subCategory": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `comments` | string |  |
| `corridorIds` | array<string> |  |
| `currentUpdate` | string |  |
| `currentUpdateDateTime` | date |  |
| `endDateTime` | date |  |
| `id` | string |  |
| `location` | string |  |
| `severity` | string |  |
| `startDateTime` | date |  |
| `status` | string |  |
| `subCategory` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Road/:ids/Disruption` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/road-disruptions.md) for the provider-specific parameters and requirements.

