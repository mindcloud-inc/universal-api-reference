# Storyblok: Get Datasource

Retrieves a Storyblok datasource by slug.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-datasource
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-datasource?connectionId=$CONNECTION_ID&datasourceId=product-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasourceId": "product-labels"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-datasource?${params}`, {
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
| `datasourceId` | string | yes | The datasource slug. Default: `product-labels`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datasource": {
        "dimensions": [
          "string"
        ],
        "id": 1,
        "name": "Ava Chen",
        "slug": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datasource` | object | The requested datasource. |
| `datasource.dimensions` | array<string> | Datasource dimensions when configured. |
| `datasource.id` | number | The datasource ID. |
| `datasource.name` | string | The datasource name. |
| `datasource.slug` | string | The datasource slug. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /datasource/:datasourceId` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datasource.md) for the provider-specific parameters and requirements.

