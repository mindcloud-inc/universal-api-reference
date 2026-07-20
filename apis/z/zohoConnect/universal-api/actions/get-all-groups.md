# Zoho Connect: Get All Groups

Retrieves all groups from Zoho Connect.

```
GET https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-groups?connectionId=$CONNECTION_ID&scopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/get-all-groups?${params}`, {
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
| `scopeId` | string | yes | Network ID. |
| `isRecentSort` | boolean | no | Sort groups by recency. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessType": "string",
      "adminUsersDetails": [
        {
          "canFollow": "string",
          "id": "string",
          "name": "Ava Chen",
          "zuid": "string"
        }
      ],
      "bgColor": "string",
      "canDelete": "string",
      "canJoin": "string",
      "clientSharedInfo": {
        "img": "string",
        "msg": "string"
      },
      "desc": "string",
      "id": "string",
      "isAdmin": "string",
      "isClosed": "string",
      "isFavourite": "string",
      "isJoined": "string",
      "isPrivate": "string",
      "isUserFollow": "string",
      "logo": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "partitionUrl": "https://example.com",
      "role": "string",
      "status": "string",
      "subType": "string",
      "time": "string",
      "type": "string",
      "typeOrd": "string",
      "url": "https://example.com",
      "userDetails": {
        "canFollow": "string",
        "id": "string",
        "name": "Ava Chen",
        "zuid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessType` | string |  |
| `adminUsersDetails[].canFollow` | string |  |
| `adminUsersDetails[].id` | string |  |
| `adminUsersDetails[].name` | string |  |
| `adminUsersDetails[].zuid` | string |  |
| `bgColor` | string |  |
| `canDelete` | string |  |
| `canJoin` | string |  |
| `clientSharedInfo.img` | string |  |
| `clientSharedInfo.msg` | string |  |
| `desc` | string |  |
| `id` | string |  |
| `isAdmin` | string |  |
| `isClosed` | string |  |
| `isFavourite` | string |  |
| `isJoined` | string |  |
| `isPrivate` | string |  |
| `isUserFollow` | string |  |
| `logo` | string |  |
| `logoUrl` | string |  |
| `name` | string |  |
| `partitionUrl` | string |  |
| `role` | string |  |
| `status` | string |  |
| `subType` | string |  |
| `time` | string |  |
| `type` | string |  |
| `typeOrd` | string |  |
| `url` | string |  |
| `userDetails.canFollow` | string |  |
| `userDetails.id` | string |  |
| `userDetails.name` | string |  |
| `userDetails.zuid` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `GET /pulse/api/allGroups` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-groups.md) for the provider-specific parameters and requirements.

