# Hopewiser: Autocomplete UK Address



```
GET https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/autocomplete-uk-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hopewiser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/autocomplete-uk-address?connectionId=$CONNECTION_ID&maf=uk-rm-paf-mr&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "maf": "uk-rm-paf-mr",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hopewiser/latest/actions/autocomplete-uk-address?${params}`, {
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
| `maf` | string | yes | Hopewiser MAF identity. This tenant is provisioned for uk-rm-paf-mr. Default: `uk-rm-paf-mr`. |
| `query` | string | yes | Autocomplete address search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expandsTo": 1,
      "isComplete": true,
      "isExpandable": true,
      "itemText": "string",
      "label1": "string",
      "label2": "string",
      "label3": "string",
      "label4": "string",
      "selected": true,
      "sid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expandsTo` | number | Approximate number of records this item expands to. |
| `isComplete` | boolean | Whether this item contains a complete address. |
| `isExpandable` | boolean | Whether this item can be expanded. |
| `itemText` | string | Display text for the returned autocomplete item. |
| `label1` | string | First formatted address label line. |
| `label2` | string | Second formatted address label line. |
| `label3` | string | Third formatted address label line. |
| `label4` | string | Fourth formatted address label line. |
| `selected` | boolean | Whether this item has been selected and output fields are present. |
| `sid` | string | Hopewiser autocomplete search identity for this result. |

## Native endpoint

Through the native Hopewiser API, this operation is `GET /autoc/json/:maf` (base URL `https://cloud.hopewiser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/autocomplete-uk-address.md) for the provider-specific parameters and requirements.

