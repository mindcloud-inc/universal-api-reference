# Umbrella: Delete Integration

Deletes an existing integration from Umbrella.

```
DELETE https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/delete-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/delete-integration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/delete-integration?${params}`, {
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
| `intId` | string | no | The integration ID. |

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

Through the native Umbrella API, this operation is `DELETE https://api.sse.cisco.com/admin/v2/integrations/:intId` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-integration.md) for the provider-specific parameters and requirements.

