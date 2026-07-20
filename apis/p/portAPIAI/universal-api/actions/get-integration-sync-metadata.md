# Port API AI: Get Integration Sync Metadata

Retrieves integration sync metadata from Port.

```
GET https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-integration-sync-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-integration-sync-metadata?connectionId=$CONNECTION_ID&integrationInternalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationInternalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/get-integration-sync-metadata?${params}`, {
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
| `integrationInternalId` | string | yes | The integration internal identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {}
      ],
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data` | array<object> |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `GET /integration/:integrationInternalId/syncsMetadata` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration-sync-metadata.md) for the provider-specific parameters and requirements.

