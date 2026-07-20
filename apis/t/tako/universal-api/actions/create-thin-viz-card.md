# Tako: Create Thin-Viz Card

Creates an embeddable Thin-Viz card in Tako.

```
POST https://connect.mindcloud.co/v1/universal/tako/latest/actions/create-thin-viz-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tako `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tako/latest/actions/create-thin-viz-card" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "components[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tako/latest/actions/create-thin-viz-card', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "components[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `components[]` | array<object> | yes | Array of Thin-Viz component configurations that define the card layout and data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "card_id": "string",
      "card_type": "string",
      "data_url": "https://example.com",
      "description": "string",
      "embed_url": "https://example.com",
      "ideal_viz_decisions": [
        {}
      ],
      "image_url": "https://example.com",
      "methodologies": [
        {}
      ],
      "relevance": "string",
      "source_indexes": [
        "string"
      ],
      "sources": [
        {}
      ],
      "title": "string",
      "visualization_data": {},
      "webpage_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `card_id` | string | Created knowledge card identifier |
| `card_type` | string | Knowledge card type |
| `data_url` | string | Underlying data URL when available |
| `description` | string | Card description |
| `embed_url` | string | Embeddable card URL |
| `ideal_viz_decisions` | array<object> | Ideal visualization decisions |
| `image_url` | string | Rendered image URL for the card |
| `methodologies` | array<object> | Methodologies used to generate the card |
| `relevance` | string | Relevance label |
| `source_indexes` | array<string> | Source index identifiers |
| `sources` | array<object> | Sources used for the card |
| `title` | string | Card title |
| `visualization_data` | object | Visualization payload |
| `webpage_url` | string | Public webpage URL for the card |

## Native endpoint

Through the native Tako API, this operation is `POST /v1/thin_viz/create/` (base URL `https://tako.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-thin-viz-card.md) for the provider-specific parameters and requirements.

