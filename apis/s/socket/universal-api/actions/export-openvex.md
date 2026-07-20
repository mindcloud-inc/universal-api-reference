# Socket: Export OpenVEX

Exports OpenVEX vulnerability data from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/export-openvex
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/export-openvex?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/export-openvex?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "author": "string",
      "lastUpdated": "string",
      "role": "string",
      "statements": [
        {
          "@id": "string",
          "actionStatement": "string",
          "actionStatementTimestamp": "string",
          "impactStatement": "string",
          "justification": "string",
          "lastUpdated": "string",
          "products": [
            {}
          ],
          "status": "string",
          "statusNotes": "string",
          "supplier": "string",
          "timestamp": "string",
          "version": 1,
          "vulnerability": {
            "@id": "string",
            "aliases": [
              "string"
            ],
            "description": "string",
            "name": "Ava Chen"
          }
        }
      ],
      "timestamp": "string",
      "tooling": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `author` | string |  |
| `lastUpdated` | string |  |
| `role` | string |  |
| `statements` | array<object> |  |
| `statements[]` | object |  |
| `statements[].@id` | string |  |
| `statements[].actionStatement` | string |  |
| `statements[].actionStatementTimestamp` | string |  |
| `statements[].impactStatement` | string |  |
| `statements[].justification` | string |  |
| `statements[].lastUpdated` | string |  |
| `statements[].products` | array<object> |  |
| `statements[].products[]` | object |  |
| `statements[].status` | string |  |
| `statements[].statusNotes` | string |  |
| `statements[].supplier` | string |  |
| `statements[].timestamp` | string |  |
| `statements[].version` | number |  |
| `statements[].vulnerability` | object |  |
| `statements[].vulnerability.@id` | string |  |
| `statements[].vulnerability.aliases` | array |  |
| `statements[].vulnerability.description` | string |  |
| `statements[].vulnerability.name` | string |  |
| `timestamp` | string |  |
| `tooling` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/export/openvex/:id` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-openvex.md) for the provider-specific parameters and requirements.

