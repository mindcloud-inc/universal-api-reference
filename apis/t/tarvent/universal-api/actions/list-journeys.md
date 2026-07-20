# Tarvent: List Journeys

Retrieves journeys from Tarvent.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-journeys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-journeys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-journeys?${params}`, {
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
      "audienceId": "string",
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "modifiedUtc": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audienceId` | string |  |
| `createdUtc` | date |  |
| `description` | string |  |
| `id` | string |  |
| `modifiedUtc` | date |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-journeys.md) for the provider-specific parameters and requirements.

