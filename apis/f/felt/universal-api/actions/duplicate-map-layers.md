# Felt: Duplicate Map Layers

Creates duplicated map layers in Felt.

```
POST https://connect.mindcloud.co/v1/universal/felt/latest/actions/duplicate-map-layers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Felt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/felt/latest/actions/duplicate-map-layers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "duplicates[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/felt/latest/actions/duplicate-map-layers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "duplicates[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `duplicates[]` | array<object> | yes | Layer duplication requests with source and destination map IDs. |

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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `layer_groups` | array<object> | Duplicated layer groups returned by the request. |
| `layers` | array<object> | Duplicated layers returned by the request. |

## Native endpoint

Through the native Felt API, this operation is `POST /duplicate_layers` (base URL `https://felt.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-map-layers.md) for the provider-specific parameters and requirements.

