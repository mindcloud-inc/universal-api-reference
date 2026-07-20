# Flexmail: List Segments

Retrieves available contact segments from Flexmail.

```
GET https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexmail/latest/actions/list-segments?${params}`, {
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
      "id": "string",
      "last_campaign_date": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number_of_contacts": 1,
      "parent_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The identifier of the segment. |
| `last_campaign_date` | date | The last campaign date for the segment when available. |
| `name` | string | The segment name. |
| `number_of_contacts` | number | The number of contacts in the segment. |
| `parent_id` | string | The parent segment identifier when present. |

## Native endpoint

Through the native Flexmail API, this operation is `GET /segments` (base URL `https://api.flexmail.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

