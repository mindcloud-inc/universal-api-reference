# Statistics Netherlands CBS: List OData V4 Catalogs

Retrieves OData V4 catalogs from Statistics Netherlands CBS.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-catalogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-catalogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/list-o-data-v4-catalogs?${params}`, {
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
      "Authority": "string",
      "ContactPoint": "string",
      "Description": "string",
      "Homepage": "string",
      "Identifier": "string",
      "Index": 1,
      "Language": "string",
      "License": "string",
      "Publisher": "string",
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Authority` | string | Authority URL. |
| `ContactPoint` | string | Contact email. |
| `Description` | string | Catalog description. |
| `Homepage` | string | Catalog homepage. |
| `Identifier` | string | Catalog identifier. |
| `Index` | number | Catalog ordering index. |
| `Language` | string | Catalog language. |
| `License` | string | License URL. |
| `Publisher` | string | Publisher URL. |
| `Title` | string | Catalog title. |

## Native endpoint

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/Catalogs` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-o-data-v4-catalogs.md) for the provider-specific parameters and requirements.

