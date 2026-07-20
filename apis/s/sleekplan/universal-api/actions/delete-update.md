# Sleekplan: Delete Update



```
DELETE https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/delete-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sleekplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/delete-update?connectionId=$CONNECTION_ID&updateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "updateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sleekplan/latest/actions/delete-update?${params}`, {
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
| `updateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "changelogId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `changelogId` | string |  |

## Native endpoint

Through the native Sleekplan API, this operation is `DELETE /update/:updateid` (base URL `https://api.sleekplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-update.md) for the provider-specific parameters and requirements.

