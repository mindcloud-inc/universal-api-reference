# City of Tampa, Florida: List Events By Type

Retrieves events by type from City of Tampa, Florida.

```
GET https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-events-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Tampa, Florida `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-events-by-type?connectionId=$CONNECTION_ID&typeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-events-by-type?${params}`, {
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
| `typeId` | string | yes | Calendar type ID or all. |

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

Through the native City of Tampa, Florida API, this operation is `GET /mobile-feeds/events/:typeId` (base URL `https://www.tampa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events-by-type.md) for the provider-specific parameters and requirements.

