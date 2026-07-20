# Basecamp: Create Document

Creates a new document in a Basecamp vault.

```
POST https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basecamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "195539477",
  "vaultId": "1069478984",
  "title": "New Hire Info",
  "content": "<div><strong>Getting started</strong></div>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "195539477",
    "vaultId": "1069478984",
    "title": "New Hire Info",
    "content": "<div><strong>Getting started</strong></div>"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Example: `195539477`. |
| `vaultId` | number | yes | Example: `1069478984`. |
| `title` | string | yes | Example: `New Hire Info`. |
| `content` | string | yes | Example: `<div><strong>Getting started</strong></div>`. |
| `status` | string | no | Default: `active`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basecamp API returns.

## Native endpoint

Through the native Basecamp API, this operation is `POST /:accountId/vaults/:vaultId/documents.json` (base URL `https://3.basecampapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

