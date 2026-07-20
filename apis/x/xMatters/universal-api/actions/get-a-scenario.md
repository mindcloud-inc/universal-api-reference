# xMatters: Get a scenario

Retrieves a scenario from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-scenario
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-scenario?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-scenario?${params}`, {
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
| `scenarioId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": {
        "count": 1,
        "data": [
          {
            "links": {
              "self": "https://example.com"
            },
            "name": "Ava Chen",
            "path": "string",
            "size": 1
          }
        ],
        "total": 1
      },
      "bypassPhoneIntro": true,
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "escalationOverride": true,
      "form": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "name": "Ava Chen",
      "overrideDeviceRestrictions": true,
      "plan": {
        "id": "string",
        "name": "Ava Chen"
      },
      "position": 1,
      "requirePhonePassword": true,
      "voicemailOptions": {
        "every": 1,
        "retry": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments.count` | number |  |
| `attachments.data[].links.self` | string |  |
| `attachments.data[].name` | string |  |
| `attachments.data[].path` | string |  |
| `attachments.data[].size` | number |  |
| `attachments.total` | number |  |
| `bypassPhoneIntro` | boolean |  |
| `created` | date |  |
| `description` | string |  |
| `escalationOverride` | boolean |  |
| `form.id` | string |  |
| `form.name` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `name` | string |  |
| `overrideDeviceRestrictions` | boolean |  |
| `plan.id` | string |  |
| `plan.name` | string |  |
| `position` | number |  |
| `requirePhonePassword` | boolean |  |
| `voicemailOptions.every` | number |  |
| `voicemailOptions.retry` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET scenarios/{scenarioId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-scenario.md) for the provider-specific parameters and requirements.

