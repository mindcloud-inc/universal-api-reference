# NeetoCal: List Available Slots

Finds available slots in NeetoCal for a scheduling link.

```
GET https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/list-available-slots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoCal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/list-available-slots?connectionId=$CONNECTION_ID&meeting_sid=string&time_zone=string&year=string&month=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meeting_sid": "string",
  "time_zone": "string",
  "year": "string",
  "month": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoCal/latest/actions/list-available-slots?${params}`, {
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
| `meeting_sid` | string | yes | The scheduling link SID. |
| `time_zone` | string | yes | IANA time zone for slot rendering. |
| `year` | string | yes | Calendar year. |
| `month` | string | yes | Calendar month. |
| `day` | string | no | Optional calendar day. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NeetoCal API returns.

## Native endpoint

Through the native NeetoCal API, this operation is `GET /meetings/:meeting_sid/slots` (base URL `https://{{credentials.subdomain}}.neetocal.com/api/external/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-slots.md) for the provider-specific parameters and requirements.

