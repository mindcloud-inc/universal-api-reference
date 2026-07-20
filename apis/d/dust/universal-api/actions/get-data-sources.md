# Dust: Get Data Sources

Retrieves data sources from a Dust space.

```
GET https://connect.mindcloud.co/v1/universal/dust/latest/actions/get-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dust `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dust/latest/actions/get-data-sources?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dust/latest/actions/get-data-sources?${params}`, {
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
| `spaceId` | string | yes | Dust space sId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataSources": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataSources` | array<object> | Data sources available in the selected Dust space. |

## Native endpoint

Through the native Dust API, this operation is `GET /api/v1/w/:workspaceId/spaces/:spaceId/data_sources` (base URL `https://dust.tt`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-sources.md) for the provider-specific parameters and requirements.

