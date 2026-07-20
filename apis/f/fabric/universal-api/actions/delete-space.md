# Fabric: Delete Space

Deletes a space from Fabric.

```
DELETE https://connect.mindcloud.co/v1/universal/fabric/latest/actions/delete-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/delete-space?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/delete-space?${params}`, {
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
| `spaceId` | string | yes | ID of the space to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Fabric API, this operation is `DELETE /v2/spaces/{spaceId}` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-space.md) for the provider-specific parameters and requirements.

