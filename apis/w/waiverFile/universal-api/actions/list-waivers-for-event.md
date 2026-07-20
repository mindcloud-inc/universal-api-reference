# WaiverFile: List Waivers for Event

Retrieves waivers for an event from WaiverFile.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waivers-for-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waivers-for-event?connectionId=$CONNECTION_ID&waiverEventID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "waiverEventID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waivers-for-event?${params}`, {
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
| `waiverEventID` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "?xml": {},
      "ArrayOfWaiver": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `?xml` | object |  |
| `ArrayOfWaiver` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetWaiversForEvent` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-waivers-for-event.md) for the provider-specific parameters and requirements.

