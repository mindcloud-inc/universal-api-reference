# Sigma: Get Connection Path



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/get-connection-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/get-connection-path?connectionId=$CONNECTION_ID&inodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/get-connection-path?${params}`, {
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
| `inodeId` | string | yes | Sigma inodeId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connectionId": "string",
      "path": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connectionId` | string | Sigma connection identifier |
| `path` | array<string> | Fully qualified connection path |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/connections/paths/{inodeId}` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-connection-path.md) for the provider-specific parameters and requirements.

