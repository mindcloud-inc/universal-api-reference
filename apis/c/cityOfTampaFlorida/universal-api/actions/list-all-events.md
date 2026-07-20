# City of Tampa, Florida: List All Events

Retrieves all events from City of Tampa, Florida.

```
GET https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-all-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Tampa, Florida `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-all-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-all-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": "string",
      "body": "string",
      "endDate": "string",
      "field_event_address": "string",
      "field_event_attachments": "string",
      "field_event_collection": "string",
      "field_event_collection_1": "string",
      "nid": "string",
      "startDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | string |  |
| `body` | string |  |
| `endDate` | string |  |
| `field_event_address` | string |  |
| `field_event_attachments` | string |  |
| `field_event_collection` | string |  |
| `field_event_collection_1` | string |  |
| `nid` | string |  |
| `startDate` | string |  |
| `title` | string |  |

## Native endpoint

Through the native City of Tampa, Florida API, this operation is `GET /mobile-feeds/events/all` (base URL `https://www.tampa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-events.md) for the provider-specific parameters and requirements.

