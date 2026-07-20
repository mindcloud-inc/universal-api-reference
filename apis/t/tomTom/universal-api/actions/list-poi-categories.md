# TomTom: List POI Categories

Retrieves available POI categories from TomTom.

```
GET https://connect.mindcloud.co/v1/universal/tomTom/latest/actions/list-poi-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TomTom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomTom/latest/actions/list-poi-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomTom/latest/actions/list-poi-categories?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "childCategoryIds": [
        1
      ],
      "id": 1,
      "name": "Ava Chen",
      "synonyms": [
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
| `childCategoryIds` | array<number> | Child category identifiers. |
| `id` | number | TomTom category identifier. |
| `name` | string | Localized category name. |
| `synonyms` | array<string> | Known category synonyms. |

## Native endpoint

Through the native TomTom API, this operation is `GET /search/2/poiCategories.json` (base URL `https://api.tomtom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-poi-categories.md) for the provider-specific parameters and requirements.

