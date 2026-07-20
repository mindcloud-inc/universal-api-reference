# OpenSanctions: Get Reconciliation Manifest



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-reconciliation-manifest
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-reconciliation-manifest?connectionId=$CONNECTION_ID&dataset=default" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dataset": "default"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-reconciliation-manifest?${params}`, {
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
| `dataset` | string | yes | Data source or collection name to scope the reconciliation manifest to. Default: `default`. Example: `default`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchSize": 1,
      "defaultTypes": [
        {}
      ],
      "documentation": "string",
      "extend": {},
      "identifierSpace": "string",
      "name": "Ava Chen",
      "preview": {},
      "schemaSpace": "string",
      "suggest": {},
      "versions": [
        "string"
      ],
      "view": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchSize` | number | Suggested batch size. |
| `defaultTypes` | array<object> | Default reconciliation entity types. |
| `documentation` | string | Provider documentation URL. |
| `extend` | object | Extension endpoint descriptors. |
| `identifierSpace` | string | Identifier namespace URL. |
| `name` | string | Manifest display name. |
| `preview` | object | Preview link template and dimensions. |
| `schemaSpace` | string | Schema namespace URL. |
| `suggest` | object | Suggestion endpoint descriptors. |
| `versions` | array<string> | Supported reconciliation API versions. |
| `view` | object | Entity view link template. |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /reconcile/:dataset` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reconciliation-manifest.md) for the provider-specific parameters and requirements.

