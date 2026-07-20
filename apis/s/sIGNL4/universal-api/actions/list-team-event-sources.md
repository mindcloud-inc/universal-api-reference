# SIGNL4: List Team Event Sources

Retrieves event sources for a team from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-event-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-event-sources?connectionId=$CONNECTION_ID&teamId=sample-team-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "sample-team-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-event-sources?${params}`, {
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
| `teamId` | string | yes | SIGNL4 team ID. Example: `sample-team-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "https://example.com",
      "description": "string",
      "disabled": true,
      "groupId": "string",
      "id": "string",
      "name": "Ava Chen",
      "options": 1,
      "subscriptionId": "string",
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
| `name` | string |  |
| `options` | number |  |
| `subscriptionId` | string |  |
| `teamId` | string |  |
| `type` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/teams/{teamId}/eventSources` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-event-sources.md) for the provider-specific parameters and requirements.

