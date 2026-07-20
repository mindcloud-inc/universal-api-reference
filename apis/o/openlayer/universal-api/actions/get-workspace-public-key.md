# Openlayer: Get Workspace Public Key

Retrieves a workspace public key from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-workspace-public-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-workspace-public-key?connectionId=$CONNECTION_ID&workspaceId=b9ef2789-e1dd-4946-9ab0-189dcee20750" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "b9ef2789-e1dd-4946-9ab0-189dcee20750"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-workspace-public-key?${params}`, {
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
| `workspaceId` | string | yes | Openlayer workspace ID. Default: `b9ef2789-e1dd-4946-9ab0-189dcee20750`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "publicKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `publicKey` | string | Workspace RSA public key. |

## Native endpoint

Through the native Openlayer API, this operation is `GET /workspaces/:workspaceId/public-key` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-public-key.md) for the provider-specific parameters and requirements.

