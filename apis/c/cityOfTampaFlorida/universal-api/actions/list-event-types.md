# City of Tampa, Florida: List Event Types

Retrieves event types from City of Tampa, Florida.

```
GET https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-event-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a City of Tampa, Florida `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-event-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/list-event-types?${params}`, {
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
      "name": "Ava Chen",
      "tid": "string",
      "vid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `tid` | string |  |
| `vid` | string |  |

## Native endpoint

Through the native City of Tampa, Florida API, this operation is `GET /taxonomy/terms/calendar_type` (base URL `https://www.tampa.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-types.md) for the provider-specific parameters and requirements.

