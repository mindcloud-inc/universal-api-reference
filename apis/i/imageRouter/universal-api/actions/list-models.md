# ImageRouter: List Models



```
GET https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ImageRouter `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imageRouter/latest/actions/list-models?${params}`, {
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
| `outputType` | string | no | Filter by output type: image or video. |
| `inputType` | string | no | Filter by supported input: image, mask, quality, size, or seconds. |
| `provider` | string | no | Filter by provider name, partial and case-insensitive. |
| `name` | string | no | Filter by model name or alias, partial and case-insensitive. |
| `free` | boolean | no | true to show only free models, false to show only paid models. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated response fields to include; id is always included. |
| `sort` | string | no | Sort by name, provider, price, or date. |
| `limit` | number | no | Maximum number of models to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": [
        [
          "string"
        ]
      ],
      "id": "string",
      "inputs": {
        "image": true,
        "mask": true,
        "quality": true,
        "seconds": [
          [
            "string"
          ]
        ],
        "size": [
          [
            "string"
          ]
        ]
      },
      "output": [
        [
          "string"
        ]
      ],
      "price": {
        "average": 1,
        "max": 1,
        "min": 1
      },
      "release_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases[]` | array<string> | Model aliases. |
| `id` | string | Model identifier. |
| `inputs` | object | Supported input capabilities. |
| `inputs.image` | boolean | Whether the model accepts input images. |
| `inputs.mask` | boolean | Whether the model accepts masks. |
| `inputs.quality` | boolean | Whether the model supports quality settings. |
| `inputs.seconds[]` | array<string> | Supported video durations. |
| `inputs.size[]` | array<string> | Supported sizes. |
| `output[]` | array<string> | Model output types. |
| `price` | object | Pricing data. |
| `price.average` | number | Average price in USD. |
| `price.max` | number | Maximum price in USD. |
| `price.min` | number | Minimum price in USD. |
| `release_date` | date | Release date when available. |

## Native endpoint

Through the native ImageRouter API, this operation is `GET /v2/models` (base URL `https://api.imagerouter.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

