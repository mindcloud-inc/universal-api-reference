# OpenSea: Get Offers By Trait

Retrieves offers for a trait in OpenSea.

```
GET https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-offers-collection-trait
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-offers-collection-trait?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSea/latest/actions/get-offers-collection-trait?${params}`, {
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
| `slug` | string | yes | Unique string to identify a collection on OpenSea |
| `type` | string | no | Trait type (deprecated: use 'traits' parameter) |
| `value` | string | no | Trait value as string (deprecated: use 'traits' parameter) |
| `floatValue` | number | no | Trait value as float (deprecated: use 'traits' parameter) |
| `intValue` | number | no | Trait value as integer (deprecated: use 'traits' parameter) |
| `traits` | string | no | JSON array of trait filters. Each trait has 'traitType' and 'value' fields. Example: [{"traitType":"Background","value":"Red"},{"traitType":"Eyes","value":"Blue"}] |
| `limit` | number | no | Number of items to return per page |
| `nextValue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `GET /api/v2/offers/collection/{slug}/traits` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offers-collection-trait.md) for the provider-specific parameters and requirements.

