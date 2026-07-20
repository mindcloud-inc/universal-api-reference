# ChartMogul: List Contacts

Retrieves contacts from ChartMogul.

```
GET https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChartMogul `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chartMogul/latest/actions/list-contacts?${params}`, {
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
      "customerExternalId": "string",
      "customerUuid": "string",
      "dataSourceUuid": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "lastSeen": "2026-05-07T12:00:00.000Z",
      "linkedIn": "https://example.com",
      "notes": "string",
      "phone": "string",
      "position": 1,
      "title": "string",
      "twitter": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerExternalId` | string |  |
| `customerUuid` | string |  |
| `dataSourceUuid` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `lastSeen` | date |  |
| `linkedIn` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `position` | number |  |
| `title` | string |  |
| `twitter` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native ChartMogul API, this operation is `GET /contacts` (base URL `https://api.chartmogul.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

