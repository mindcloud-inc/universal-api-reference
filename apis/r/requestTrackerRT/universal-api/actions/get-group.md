# Request Tracker (RT): Get Group

Retrieves a group from Request Tracker.

```
GET https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Request Tracker (RT) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/requestTrackerRT/latest/actions/get-group?${params}`, {
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
| `groupId` | string | yes | The RT group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "disabled": "string",
      "domain": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `disabled` | string |  |
| `domain` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Request Tracker (RT) API, this operation is `GET group/:groupId` (base URL `https://try.requesttracker.io/sufongepl_57381/REST/2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

