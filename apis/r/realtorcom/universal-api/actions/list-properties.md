# Realtor.com: List Properties



```
GET https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realtor.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/list-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/list-properties?${params}`, {
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
| `filter` | string | no | Optional OData filter expression. ListHub documents supported fields including PropertyType, ListingId, ModificationTimestamp, StandardStatus, SourceSystemID, PostalCode, Country, ListingKey, ListPrice, PropertySubType, StateOrProvince, and TransactionType. Example: `StandardStatus eq 'Active'`. |
| `select` | string | no | Comma-separated RESO field names to return, for example ListingKey,StandardStatus,ListPrice. Example: `ListingKey,StandardStatus,ListPrice`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderby` | string | no | Optional OData order expression. ListHub documents ordering on ListingKey and ModificationTimestamp only. Example: `ListingKey asc`. |
| `count` | boolean | no | Set true to request an @odata.count value when supported for the query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "count": 1,
        "nextLink": "https://example.com"
      },
      "value": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string | OData context URL for the property collection response. |
| `@odata.count` | number | Total matching property count when $count=true is requested. |
| `@odata.nextLink` | string | OData URL for the next page when more property records are available. |
| `value` | array<object> | Array of Property records returned by ListHub. Fields depend on $select and include ListingKey, ListingId, PropertyType, PropertySubType, StandardStatus, ListPrice, UnparsedAddress, and ModificationTimestamp in the verified projection. |

## Native endpoint

Through the native Realtor.com API, this operation is `GET /odata/Property` (base URL `https://api.listhub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

