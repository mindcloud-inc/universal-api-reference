# Transport for London: Get Line Disruptions

Retrieves disruptions for selected lines in Transport for London.

```
GET https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-disruptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transport for London `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-disruptions?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/transportForLondon/latest/actions/line-disruptions?${params}`, {
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
| `ids` | string | yes | Comma-separated TfL line IDs, such as victoria,circle. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `created` | date |  |
| `description` | string |  |
| `lastUpdate` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Transport for London API, this operation is `GET /Line/:ids/Disruption` (base URL `https://api.tfl.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/line-disruptions.md) for the provider-specific parameters and requirements.

