# Google Chat: List Spaces

Retrieves Google Chat spaces the caller is a member of.

```
GET https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-spaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-spaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/list-spaces?${params}`, {
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
| `filter` | string | no | Optional. Filter spaces by supported Google Chat space fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTime": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "displayName": "Ava Chen",
      "lastActiveTime": "2026-05-07T12:00:00.000Z",
      "membershipCount": {},
      "name": "Ava Chen",
      "spaceHistoryState": "string",
      "spaceThreadingState": "string",
      "spaceType": "string",
      "spaceUri": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTime` | date |  |
| `customer` | string |  |
| `displayName` | string |  |
| `lastActiveTime` | date |  |
| `membershipCount` | object |  |
| `name` | string |  |
| `spaceHistoryState` | string |  |
| `spaceThreadingState` | string |  |
| `spaceType` | string |  |
| `spaceUri` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Chat API, this operation is `GET /spaces` (base URL `https://chat.googleapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spaces.md) for the provider-specific parameters and requirements.

