# Booqable: Get Product Availability

Retrieves availability for a product in Booqable.

```
GET https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-product-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Booqable `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-product-availability?connectionId=$CONNECTION_ID&limit=25&offset=0&month=4&year=2026&productId=6774b37c-a832-4868-8ae9-b9c90cb5c75e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "month": "4",
  "year": "2026",
  "productId": "6774b37c-a832-4868-8ae9-b9c90cb5c75e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/booqable/latest/actions/get-product-availability?${params}`, {
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
| `month` | number | yes | Calendar month to inspect. Example: `4`. |
| `year` | number | yes | Calendar year to inspect. Example: `2026`. |
| `productId` | string | yes | Product UUID to evaluate for booking availability. Example: `6774b37c-a832-4868-8ae9-b9c90cb5c75e`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields.availabilities` | string | no | Comma-separated availability fields to include instead of the default fields. Example: `subject_type,subject_id,date,status,available`. |
| `meta.total[]` | array<string> | no | Aggregations to include in meta.total. Example: `count`. |
| `day` | number | no | Day of the month for time-based availability. Example: `10`. |
| `startsAt` | date | no | Start timestamp for time-based availability. Example: `2026-04-10 09:00:00`. |
| `durationPeriod` | string | no | Time-slot duration period for day views. Example: `day`. |
| `interval` | number | no | Minute interval for time-based availability. Example: `60`. |
| `useBusinessHours` | boolean | no | Limit time-based results to business hours. Example: `true`. |
| `locationId` | string | no | Location UUID to scope the availability query. Example: `158d5e18-4cbe-4e0b-8bc7-647b95797e14`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Availability details such as date, status, subject, and time granularity. |
| `id` | string | Unique identifier for the availability record. |
| `type` | string | Resource type, always availabilities. |

## Native endpoint

Through the native Booqable API, this operation is `GET /availabilities` (base URL `https://mindcloud.booqable.com/api/4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-product-availability.md) for the provider-specific parameters and requirements.

