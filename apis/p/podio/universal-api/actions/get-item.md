# Podio: Get Item

Retrieves an existing item from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-item?${params}`, {
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
| `itemId` | number | yes | The id of the item. Example: `123456789`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `markAsViewed` | boolean | no | True to mark the item as viewed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {},
      "appItemId": 1,
      "appItemIdFormatted": "string",
      "comments": [
        {}
      ],
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "currentRevision": {},
      "externalId": "string",
      "fields": [
        {}
      ],
      "files": [
        {}
      ],
      "initialRevision": {},
      "invite": {},
      "isLiked": true,
      "itemId": 1,
      "lastEventOn": "2026-05-07T12:00:00.000Z",
      "likeCount": 1,
      "link": "https://example.com",
      "linkedAccountData": {},
      "linkedAccountId": 1,
      "participants": {},
      "presence": {},
      "priority": 1,
      "push": {},
      "ratings": {},
      "recurrence": {},
      "ref": {},
      "refs": [
        {}
      ],
      "reminder": {},
      "revision": 1,
      "revisions": [
        {}
      ],
      "rights": [
        "string"
      ],
      "sharefileVaultFolderId": 1,
      "sharefileVaultUrl": "https://example.com",
      "subscribed": true,
      "subscribedCount": 1,
      "tags": [
        "string"
      ],
      "title": "string",
      "userRatings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `app` | object |  |
| `appItemId` | number |  |
| `appItemIdFormatted` | string |  |
| `comments` | array<object> |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `currentRevision` | object |  |
| `externalId` | string |  |
| `fields` | array<object> |  |
| `files` | array<object> |  |
| `initialRevision` | object |  |
| `invite` | object |  |
| `isLiked` | boolean |  |
| `itemId` | number |  |
| `lastEventOn` | date |  |
| `likeCount` | number |  |
| `link` | string |  |
| `linkedAccountData` | object |  |
| `linkedAccountId` | number |  |
| `participants` | object |  |
| `presence` | object |  |
| `priority` | number |  |
| `push` | object |  |
| `ratings` | object |  |
| `recurrence` | object |  |
| `ref` | object |  |
| `refs` | array<object> |  |
| `reminder` | object |  |
| `revision` | number |  |
| `revisions` | array<object> |  |
| `rights` | array<string> |  |
| `sharefileVaultFolderId` | number |  |
| `sharefileVaultUrl` | string |  |
| `subscribed` | boolean |  |
| `subscribedCount` | number |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `userRatings` | object |  |

## Native endpoint

Through the native Podio API, this operation is `GET /item/:item_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

