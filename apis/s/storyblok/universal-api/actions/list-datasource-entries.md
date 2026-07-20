# Storyblok: List Datasource Entries

Retrieves datasource entries from Storyblok by datasource.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-datasource-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-datasource-entries?connectionId=$CONNECTION_ID&limit=25&offset=0&datasource=product-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "datasource": "product-labels"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/list-datasource-entries?${params}`, {
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
| `datasource` | string | yes | The datasource slug to read entries from. Default: `product-labels`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cv": 1,
      "datasource_entries": [
        {
          "dimension_value": "string",
          "id": 1,
          "name": "Ava Chen",
          "value": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cv` | number | The cache version. |
| `datasource_entries` | array<object> | Entries for the requested datasource. |
| `datasource_entries[].dimension_value` | string | The dimension value when present. |
| `datasource_entries[].id` | number | The datasource entry ID. |
| `datasource_entries[].name` | string | The datasource entry name. |
| `datasource_entries[].value` | string | The datasource entry value. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /datasource_entries` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-datasource-entries.md) for the provider-specific parameters and requirements.

