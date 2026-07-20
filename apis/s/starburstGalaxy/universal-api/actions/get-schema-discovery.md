# Starburst Galaxy: Get schema discovery



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-schema-discovery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-schema-discovery?connectionId=$CONNECTION_ID&schemaDiscoveryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaDiscoveryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/get-schema-discovery?${params}`, {
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
| `schemaDiscoveryId` | string | yes | Starburst Galaxy schema discovery ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catalogId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "errors": [
        "string"
      ],
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "schemaDiscoveryId": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catalogId` | string | Catalog ID. |
| `createdAt` | date | Time when schema discovery was created. |
| `errors` | array<string> | Errors that prevented schema discovery from finishing. |
| `finishedAt` | date | Time when schema discovery finished. |
| `schemaDiscoveryId` | string | Schema discovery ID. |
| `startedAt` | date | Time when schema discovery started. |
| `status` | string | Schema discovery status. |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/schemaDiscovery/{schemaDiscoveryId}` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schema-discovery.md) for the provider-specific parameters and requirements.

