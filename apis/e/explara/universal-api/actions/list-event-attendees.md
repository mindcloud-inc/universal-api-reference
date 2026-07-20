# Explara: List Event Attendees

Retrieves event attendees from Explara.

```
GET https://connect.mindcloud.co/v1/universal/explara/latest/actions/list-event-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/explara/latest/actions/list-event-attendees?connectionId=$CONNECTION_ID&eventId=string&fromRecord=1&toRecord=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "fromRecord": "1",
  "toRecord": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/explara/latest/actions/list-event-attendees?${params}`, {
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
| `eventId` | string | yes | Explara event identifier. |
| `fromRecord` | number | yes | Starting attendee record number. |
| `toRecord` | number | yes | Ending attendee record number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Explara API returns.

## Native endpoint

Through the native Explara API, this operation is `POST /api/e/attendee-list` (base URL `https://www.explara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-attendees.md) for the provider-specific parameters and requirements.

