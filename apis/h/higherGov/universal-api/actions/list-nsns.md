# HigherGov: List NSNs

Retrieves national stock numbers from HigherGov.

```
GET https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-nsns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HigherGov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-nsns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/higherGov/latest/actions/list-nsns?${params}`, {
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
| `cageCode` | string | no | Supplier CAGE |
| `nsn` | string | no | National Stock Number |
| `partNumber` | string | no | Part number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awards": "string",
      "fsc": "string",
      "niin": "string",
      "nomenclature": "string",
      "nsn": "string",
      "opp_count": 1,
      "part_numbers": "string",
      "suppliers": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awards` | string |  |
| `fsc` | string |  |
| `niin` | string |  |
| `nomenclature` | string |  |
| `nsn` | string |  |
| `opp_count` | number |  |
| `part_numbers` | string |  |
| `suppliers` | string |  |

## Native endpoint

Through the native HigherGov API, this operation is `GET /api-external/nsn/` (base URL `https://www.highergov.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nsns.md) for the provider-specific parameters and requirements.

