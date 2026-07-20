# Zoho Connect: Get My Boards

Retrieves your boards from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-my-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-my-boards?connectionId=$CONNECTION_ID&scopeID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-my-boards?${params}`, {
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
| `boardsModifiedTime` | number | no | Fetch boards modified after this Unix timestamp in milliseconds. |
| `scopeID` | string | yes | ID of the network to fetch boards from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "myBoards": {
        "boards": [
          {}
        ],
        "boardsModifiedTime": "string",
        "defaultPriority": [
          {}
        ],
        "defaultStatus": [
          {}
        ],
        "privateUserTags": [
          {}
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `myBoards.boards` | array<object> |  |
| `myBoards.boardsModifiedTime` | string |  |
| `myBoards.defaultPriority` | array<object> |  |
| `myBoards.defaultStatus` | array<object> |  |
| `myBoards.privateUserTags` | array<object> |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/myBoards` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-my-boards.md) for the provider-specific parameters and requirements.

