# SIGNL4: Get Event Source

Retrieves an event source from SIGNL4 by ID.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-source?connectionId=$CONNECTION_ID&eventSourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventSourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-event-source?${params}`, {
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
| `eventSourceId` | string | yes | Id of the event source. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | number | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "description": "string",
      "disabled": true,
      "groupId": "string",
      "id": "string",
      "lastEvent": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "options": 1,
      "subscriptionId": "string",
      "subType": "string",
      "teamId": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `description` | string |  |
| `disabled` | boolean |  |
| `groupId` | string |  |
| `id` | string |  |
| `lastEvent` | date |  |
| `name` | string |  |
| `options` | number |  |
| `subscriptionId` | string |  |
| `subType` | string |  |
| `teamId` | string |  |
| `type` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/eventsources/{eventSourceId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-source.md) for the provider-specific parameters and requirements.

