# QuickFile: Search Events



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-events?${params}`, {
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
| `returnCount` | number | no | Maximum number of QuickFile events to return. Default: `25`. |
| `continuationToken` | string | no | Continuation token from a previous partial QuickFile event search response. |
| `fromDateTime` | date | no | Start of the event search range. |
| `toDateTime` | date | no | End of the event search range. |
| `searchType` | string | no | Optional QuickFile entity type to scope the event search. One of: `0`, `1`, `2`, `3`. |
| `refId` | string | no | Entity identifier used with SearchType. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventTime": "2026-05-07T12:00:00.000Z",
      "loginUser": "string",
      "note": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventTime` | date | Date and time the QuickFile system event was recorded. |
| `loginUser` | string | User or system identity associated with the event. |
| `note` | string | Human-readable event description from the QuickFile audit log. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /system/searchevents` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-events.md) for the provider-specific parameters and requirements.

