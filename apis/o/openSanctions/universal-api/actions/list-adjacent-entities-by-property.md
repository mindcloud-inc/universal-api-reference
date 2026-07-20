# OpenSanctions: List Adjacent Entities By Property



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-adjacent-entities-by-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-adjacent-entities-by-property?connectionId=$CONNECTION_ID&limit=25&offset=0&entity_id=Q7747&property_name=associations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "entity_id": "Q7747",
  "property_name": "associations"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/list-adjacent-entities-by-property?${params}`, {
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
| `entity_id` | string | yes | ID of the entity whose graph context is requested. Default: `Q7747`. |
| `property_name` | string | yes | Adjacent relationship or property group to fetch for the entity. Default: `associations`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": 1,
      "offset": 1,
      "results": [
        {}
      ],
      "total": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Number of adjacent results requested. |
| `offset` | number | Offset of adjacent results. |
| `results` | array<object> | Adjacent relationship/entity records for the selected property. |
| `total` | object | Total adjacent result metadata. |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /entities/:entity_id/adjacent/:property_name` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-adjacent-entities-by-property.md) for the provider-specific parameters and requirements.

