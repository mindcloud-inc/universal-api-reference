# Faithlife: Get Group

Retrieves a group from Faithlife.

```
GET https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Faithlife `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-group?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/faithlife/latest/actions/get-group?${params}`, {
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
| `groupId` | string | yes | The Faithlife group ID or token to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "avatarUrls": {},
      "groupId": "string",
      "isPinned": true,
      "kind": "string",
      "name": "Ava Chen",
      "preferredMembershipKind": "string",
      "privacy": "string",
      "timeZone": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `avatarUrls` | object |  |
| `groupId` | string |  |
| `isPinned` | boolean |  |
| `kind` | string |  |
| `name` | string |  |
| `preferredMembershipKind` | string |  |
| `privacy` | string |  |
| `timeZone` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Faithlife API, this operation is `GET /groups/:groupId` (base URL `https://accountsapi.logos.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

