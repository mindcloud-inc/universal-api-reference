# Vercel: Delete Alias

Deletes an existing alias from Vercel.

```
DELETE https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vercel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-alias?connectionId=$CONNECTION_ID&aliasId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aliasId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vercel/latest/actions/delete-alias?${params}`, {
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
| `aliasId` | string | yes | The alias ID or alias string to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Vercel API, this operation is `DELETE /v2/aliases/:aliasId` (base URL `https://api.vercel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-alias.md) for the provider-specific parameters and requirements.

