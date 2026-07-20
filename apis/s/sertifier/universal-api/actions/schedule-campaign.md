# Sertifier: Schedule Campaign

Schedules an existing campaign in Sertifier.

```
PUT https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/schedule-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/schedule-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "Campaign ID",
  "publishDate": "2026-03-24 16:00"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/schedule-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "Campaign ID",
    "publishDate": "2026-03-24 16:00"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `Campaign ID`. |
| `publishDate` | string | yes | Example: `2026-03-24 16:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": true,
      "hasError": true,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | boolean |  |
| `hasError` | boolean |  |
| `message` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `POST /campaign/schedule` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-campaign.md) for the provider-specific parameters and requirements.

