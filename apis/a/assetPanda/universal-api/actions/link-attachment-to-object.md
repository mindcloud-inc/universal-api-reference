# Asset Panda: Link Attachment to Object

Links an attachment to an object in Asset Panda.

```
PUT https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/link-attachment-to-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Panda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/link-attachment-to-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assetPanda/latest/actions/link-attachment-to-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupObjectId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asset Panda API returns.

## Native endpoint

Through the native Asset Panda API, this operation is `POST /v3/group/objects/:groupObjectId/attachments` (base URL `https://api.assetpanda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-attachment-to-object.md) for the provider-specific parameters and requirements.

