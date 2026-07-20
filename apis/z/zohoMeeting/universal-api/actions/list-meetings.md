# Zoho Meeting: List Meetings

Retrieves meetings from Zoho Meeting.

```
GET https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Meeting `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-meetings?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=%7B%7Bcredentials.organizationId%7D%7D&listType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizationId": "{{credentials.organizationId}}",
  "listType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMeeting/latest/actions/list-meetings?${params}`, {
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
| `organizationId` | string | yes | Organization ID (zsoid) from Get Current User Details. Default: `{{credentials.organizationId}}`. |
| `listType` | string | yes | Meeting list type: all, past, today, or upcoming. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "isMettingSessionAvailable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `isMettingSessionAvailable` | boolean |  |

## Native endpoint

Through the native Zoho Meeting API, this operation is `GET /api/v2/:organizationId/sessions.json` (base URL `https://meeting.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

