# Pushover: Get Group



```
GET https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-group?connectionId=$CONNECTION_ID&group=Pushover%20group%20key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "Pushover group key"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/get-group?${params}`, {
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
| `group` | string | yes | Key of the group to retrieve. Example: `Pushover group key`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "users": [
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
| `name` | string | Group name. |
| `users` | array<object> | Members of the group. |

## Native endpoint

Through the native Pushover API, this operation is `GET /groups/:group.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

