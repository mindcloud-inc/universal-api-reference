# xMatters: Get a shift

Retrieves a shift from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-shift
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-shift?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-shift?${params}`, {
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
| `groupId` | string | no |  |
| `shiftId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "group": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "targetName": "Ava Chen"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "notifyEndOfEscalation": {
        "notifyEnabled": "string"
      },
      "repeatEscalation": {
        "repeatEnabled": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `group.id` | string |  |
| `group.links.self` | string |  |
| `group.targetName` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `notifyEndOfEscalation.notifyEnabled` | string |  |
| `repeatEscalation.repeatEnabled` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET groups/{groupId}/shifts/{shiftId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-shift.md) for the provider-specific parameters and requirements.

