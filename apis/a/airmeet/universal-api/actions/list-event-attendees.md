# Airmeet: List Event Attendees

Finds event attendance records in Airmeet.

```
GET https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-event-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-event-attendees?connectionId=$CONNECTION_ID&airmeetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "airmeetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-event-attendees?${params}`, {
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
| `after` | string | no | Fetch attendees after this cursor. |
| `airmeetId` | string | yes | The Airmeet event ID. |
| `before` | string | no | Fetch attendees before this cursor. |
| `size` | number | no | Number of attendees to return per page, between 1 and 50. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `GET /airmeet/{airmeetId}/attendees` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-attendees.md) for the provider-specific parameters and requirements.

