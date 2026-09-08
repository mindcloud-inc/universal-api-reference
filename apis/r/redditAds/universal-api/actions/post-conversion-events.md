# Reddit Ads: Post Conversion Events

Creates conversion events for a Reddit pixel.

```
POST https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/post-conversion-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reddit Ads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/post-conversion-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pixelId": "string",
  "data": {},
  "data.events[]": [
    {}
  ],
  "data.events[].eventAt": "Select event time",
  "data.events[].actionSource": "APP",
  "data.events[].type": {},
  "data.events[].type.trackingType": "ADD_TO_CART"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/post-conversion-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pixelId": "string",
    "data": {},
    "data.events[]": [{}],
    "data.events[].eventAt": "Select event time",
    "data.events[].actionSource": "APP",
    "data.events[].type": {},
    "data.events[].type.trackingType": "ADD_TO_CART"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pixelId` | string | yes | Reddit Ads pixel identifier. |
| `data` | object | yes | JSON request body from the Reddit Ads API spec. |
| `data.events[]` | array<object> | yes | One or more conversion events; Reddit accepts up to 1,000 events per request. |
| `data.events[].eventAt` | date | yes | Unix epoch timestamp in milliseconds when the conversion occurred. Example: `Select event time`. |
| `data.events[].actionSource` | list<string> | yes | Channel where the conversion occurred. One of: `APP`, `OTHER`, `PHYSICAL_STORE`, `WEBSITE`. |
| `data.events[].type` | object | yes |  |
| `data.events[].type.trackingType` | list<string> | yes | Reddit standard conversion type, or CUSTOM for a custom event. One of: `ADD_TO_CART`, `ADD_TO_WISHLIST`, `CUSTOM`, `LEAD`, `PAGE_VISIT`, `PURCHASE`, `SEARCH`, `SIGN_UP`, `VIEW_CONTENT`. |
| `data.events[].type.customEventName` | string | no | Enter a name when Conversion Event is Custom, for example DemoBooked or TrialStarted. Leave blank for standard Reddit events. Example: `DemoBooked`. |
| `data.events[].metadata` | object | no | Optional conversion metadata used for deduplication and revenue reporting. |
| `data.events[].metadata.conversionId` | string | no | Unique event ID used to deduplicate Pixel and CAPI events. Example: `Order or event ID`. |
| `data.events[].metadata.currency` | string | no | ISO 4217 currency code for revenue-related events. Example: `USD`. |
| `data.events[].metadata.value` | number | no | Transaction value in the currency's base unit. Example: `10.99`. |
| `data.events[].metadata.itemCount` | number | no | Total number of items for a revenue-related event. Example: `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.testId` | string | no | Optional Reddit Events Manager test ID. Leave blank for production events. Example: `t2_...`. |
| `data.events[].clickId` | string | no | Reddit click ID (`rdt_cid`) used to improve attribution. Example: `3184742045291813272`. |
| `data.events[].eventSourceUrl` | string | no | URL where a WEBSITE conversion occurred; include `rdt_cid` when available. Example: `https://example.com/checkout`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Conversion event identifier. |
| `status` | string | Conversion event status. |

## Native endpoint

Through the native Reddit Ads API, this operation is `POST /pixels/:pixel_id/conversion_events` (base URL `https://ads-api.reddit.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-conversion-events.md) for the provider-specific parameters and requirements.

