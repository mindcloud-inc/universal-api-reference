# Realtor.com: Sync Properties



```
GET https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/sync-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realtor.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/sync-properties?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/sync-properties?${params}`, {
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
| `filter` | string | no | Optional OData filter expression. ListHub recommends Sync for ListingKey and ModificationTimestamp comparison. Example: `StandardStatus eq 'Active'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "count": 1
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
| `@odata.count` | number | Total number of records matching the Sync request filter. |
| `value` | array<object> | Array of sync records. ListHub documents and runtime confirms each item contains ListingKey and ModificationTimestamp. |

## Native endpoint

Through the native Realtor.com API, this operation is `GET /odata/Sync` (base URL `https://api.listhub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-properties.md) for the provider-specific parameters and requirements.

