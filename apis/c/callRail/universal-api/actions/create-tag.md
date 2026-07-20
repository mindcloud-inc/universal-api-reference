# CallRail: Create Tag

Creates a tag in CallRail.

```
POST https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callRail/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | string | yes |  |
| `name` | string | yes |  |
| `company_id` | string | no |  |
| `color` | string | no |  |
| `tag_level` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backgroundColor": "string",
      "color": "string",
      "companyId": "string",
      "createdAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "tagLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backgroundColor` | string |  |
| `color` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |
| `tagLevel` | string |  |

## Native endpoint

Through the native CallRail API, this operation is `POST /v3/a/:account_id/tags.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

