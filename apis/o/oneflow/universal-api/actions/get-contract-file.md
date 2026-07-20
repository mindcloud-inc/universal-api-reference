# Oneflow: Get Contract File

Retrieves contract file details from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contract-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contract-file?connectionId=$CONNECTION_ID&contractId=string&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contractId": "string",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-contract-file?${params}`, {
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
| `contractId` | string | yes | The Oneflow contract ID. |
| `fileId` | string | yes | The Oneflow contract file ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extension": "string",
      "id": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extension` | string |  |
| `id` | number |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /contracts/:contractId/files/:fileId` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contract-file.md) for the provider-specific parameters and requirements.

