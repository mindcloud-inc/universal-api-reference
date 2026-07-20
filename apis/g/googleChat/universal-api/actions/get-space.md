# Google Chat: Get Space

Retrieves details about a Google Chat space.

```
GET https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/get-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/get-space?connectionId=$CONNECTION_ID&space=4Oe1TyAAAAE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "space": "4Oe1TyAAAAE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleChat/latest/actions/get-space?${params}`, {
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
| `space` | string | yes | Enter only the space ID from the List Spaces result. If the result shows spaces/4Oe1TyAAAAE, enter 4Oe1TyAAAAE here. Example: `4Oe1TyAAAAE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessSettings": {},
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
| `accessSettings` | object |  |
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

Through the native Google Chat API, this operation is `GET /spaces/:space` (base URL `https://chat.googleapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space.md) for the provider-specific parameters and requirements.

