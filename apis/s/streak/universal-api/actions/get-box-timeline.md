# Streak: Get Box Timeline

Retrieves timeline entries for a box in Streak.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-box-timeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-box-timeline?connectionId=$CONNECTION_ID&boxKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boxKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/get-box-timeline?${params}`, {
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
| `boxKey` | string | yes | The key of the box to get the timeline for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filters` | list<string> | no | The timeline entity types to include. One of: `CALL_LOGS`, `COMMENTS`, `EMAILS`, `FILES`, `HANGOUTS_CHAT`, `MEETING_NOTES`, `NEWSFEED_BOX_CREATION_MOVE`, `NEWSFEED_BOX_EDIT`. Accepts multiple values as an array. |
| `direction` | list<string> | no | Whether to return results in ascending or descending timestamp order. One of: `Ascending`, `Descending`. |
| `startTimestamp` | number | no | The timestamp boundary for returned results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
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
| `entries` | array<object> |  |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v2/boxes/:boxKey/timeline` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-box-timeline.md) for the provider-specific parameters and requirements.

