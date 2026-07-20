# Podio: Add Item

Creates a new item in Podio.

```
POST https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "123456789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/add-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "123456789"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | number | yes | The id of the app to add the item to. Example: `123456789`. |
| `fields` | object | no | Field values keyed by field id or external id. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hook` | boolean | no | True to run item hooks. |
| `silent` | boolean | no | True to suppress notifications. |
| `externalId` | string | no | Unique external id for the item. Example: `external-item-001`. |
| `fileIds[]` | array<number> | no | Files to attach to the item. Example: `12345`. |
| `tags[]` | array<string> | no | Tags to add to the item. Example: `priority`. |
| `reminder` | object | no | Reminder configuration for the item. |
| `recurrence` | object | no | Recurrence settings for the item. |
| `linkedAccountId` | number | no | Linked account id to use when creating the item. Example: `12345`. |
| `ref` | object | no | Reference object used for ratings or app auth. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "app": {},
      "appItemId": 1,
      "appItemIdFormatted": "string",
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "currentRevision": {},
      "externalId": "string",
      "fields": [
        {}
      ],
      "initialRevision": {},
      "itemId": 1,
      "lastEventOn": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "linkedAccountData": {},
      "linkedAccountId": 1,
      "participants": {},
      "presence": {},
      "priority": 1,
      "push": {},
      "recurrence": {},
      "ref": {},
      "reminder": {},
      "revision": 1,
      "rights": [
        "string"
      ],
      "sharefileVaultFolderId": 1,
      "sharefileVaultUrl": "https://example.com",
      "subscribedCount": 1,
      "title": "string"
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
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `currentRevision` | object |  |
| `externalId` | string |  |
| `fields` | array<object> |  |
| `initialRevision` | object |  |
| `itemId` | number |  |
| `lastEventOn` | date |  |
| `link` | string |  |
| `linkedAccountData` | object |  |
| `linkedAccountId` | number |  |
| `participants` | object |  |
| `presence` | object |  |
| `priority` | number |  |
| `push` | object |  |
| `recurrence` | object |  |
| `ref` | object |  |
| `reminder` | object |  |
| `revision` | number |  |
| `rights` | array<string> |  |
| `sharefileVaultFolderId` | number |  |
| `sharefileVaultUrl` | string |  |
| `subscribedCount` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Podio API, this operation is `POST /item/app/:app_id/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-item.md) for the provider-specific parameters and requirements.

