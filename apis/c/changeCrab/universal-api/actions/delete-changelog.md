# ChangeCrab: Delete Changelog

Deletes an existing changelog from ChangeCrab.

```
DELETE https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/delete-changelog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChangeCrab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/delete-changelog?connectionId=$CONNECTION_ID&id=e.g.%20product-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. product-updates"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/delete-changelog?${params}`, {
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
| `id` | string | yes | The ChangeCrab changelog access ID. Example: `e.g. product-updates`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ChangeCrab API, this operation is `DELETE /changelogs/:id` (base URL `https://changecrab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-changelog.md) for the provider-specific parameters and requirements.

