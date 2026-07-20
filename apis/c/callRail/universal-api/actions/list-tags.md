# CallRail: List Tags

Retrieves tags from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-tags?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/list-tags?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |

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

Through the native CallRail API, this operation is `GET /v3/a/:account_id/tags.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

