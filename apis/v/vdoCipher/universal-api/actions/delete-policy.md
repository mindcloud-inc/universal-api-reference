# VdoCipher: Delete Policy

Deletes an existing policy from VdoCipher.

```
DELETE https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/delete-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VdoCipher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/delete-policy?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vdoCipher/latest/actions/delete-policy?${params}`, {
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
| `id` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native VdoCipher API, this operation is `DELETE /policy/:id` (base URL `https://dev.vdocipher.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-policy.md) for the provider-specific parameters and requirements.

