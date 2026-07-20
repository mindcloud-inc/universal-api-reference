# Statistics Netherlands CBS: Get OData V4 Catalog

Retrieves an OData V4 catalog from Statistics Netherlands CBS.

```
GET https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statistics Netherlands CBS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-catalog?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-o-data-v4-catalog?${params}`, {
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
| `identifier` | string | yes | CBS OData v4 catalog identifier, such as CBS. |

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

Through the native Statistics Netherlands CBS API, this operation is `GET https://datasets.cbs.nl/odata/v1/CBS/Catalogs('{{identifier}}')` (base URL `https://opendata.cbs.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-o-data-v4-catalog.md) for the provider-specific parameters and requirements.

