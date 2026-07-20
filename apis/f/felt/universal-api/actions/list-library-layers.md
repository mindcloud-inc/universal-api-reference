# Felt: List Library Layers

Retrieves library layers from Felt.

```
GET https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-library-layers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-library-layers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/felt/latest/actions/list-library-layers?${params}`, {
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
| `source` | list | no | Which Felt library source to list. One of: `All`, `Felt`, `Workspace`. Default: `all`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "layer_groups": [
        {}
      ],
      "layers": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `layer_groups` | array<object> | Library layer groups. |
| `layers` | array<object> | Library layers. |
| `type` | string | Library payload type. |

## Native endpoint

Through the native Felt API, this operation is `GET /library` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-library-layers.md) for the provider-specific parameters and requirements.

