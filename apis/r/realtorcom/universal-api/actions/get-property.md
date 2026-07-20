# Realtor.com: Get Property



```
GET https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/get-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realtor.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/get-property?connectionId=$CONNECTION_ID&listingKey=3yd-FAKE-1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listingKey": "3yd-FAKE-1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realtorcom/latest/actions/get-property?${params}`, {
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
| `listingKey` | string | yes | Unique ListHub ListingKey, for example 3yd-FAKE-1. Example: `3yd-FAKE-1`. |
| `select` | string | no | Comma-separated RESO field names to return for the listing. Example: `ListingKey,StandardStatus,ListPrice`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@odata": {
        "context": "string",
        "id": "string"
      },
      "ListingId": "string",
      "ListingKey": "string",
      "ListPrice": 1,
      "ModificationTimestamp": "string",
      "PropertySubType": "string",
      "PropertyType": "string",
      "StandardStatus": "string",
      "UnparsedAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@odata.context` | string | OData context URL for the single Property response. |
| `@odata.id` | string | OData entity self-link for the property record. |
| `ListingId` | string | Listing identifier from the source feed. |
| `ListingKey` | string | Unique ListHub listing key used as the primary identifier. |
| `ListPrice` | number | Listing price. |
| `ModificationTimestamp` | string | Last modification timestamp for the property record. |
| `PropertySubType` | string | Property subtype. |
| `PropertyType` | string | High-level property type. |
| `StandardStatus` | string | Standard listing status. |
| `UnparsedAddress` | string | Display address when available from the feed. |

## Native endpoint

Through the native Realtor.com API, this operation is `GET /odata/Property('{{listingKey}}')` (base URL `https://api.listhub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property.md) for the provider-specific parameters and requirements.

