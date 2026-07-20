# Storerocket: Delete Location



```
DELETE https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/delete-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storerocket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/delete-location?connectionId=$CONNECTION_ID&projectId=string&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storerocket/latest/actions/delete-location?${params}`, {
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
| `projectId` | string | yes | The StoreRocket project ID that owns the location. |
| `locationId` | string | yes | The StoreRocket location ID. |

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

Through the native Storerocket API, this operation is `DELETE /projects/:projectId/locations/:locationId` (base URL `https://storerocket.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-location.md) for the provider-specific parameters and requirements.

