# Resource Guru: Delete Resource

Deletes an existing resource from Resource Guru.

```
DELETE https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/delete-resource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resource Guru `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/delete-resource?connectionId=$CONNECTION_ID&id=900584" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "900584"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resourceGuru/latest/actions/delete-resource?${params}`, {
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
| `id` | number | yes | Resource ID. Default: `900584`. Example: `900584`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | ID of the deleted resource supplied in the request. |

## Native endpoint

Through the native Resource Guru API, this operation is `DELETE /resources/:id` (base URL `https://api.resourceguruapp.com/v1/{{credentials.accountId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-resource.md) for the provider-specific parameters and requirements.

