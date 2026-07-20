# ECAL: Search Batch Private Events By IDs

Finds batch private ECAL events by event IDs.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/search-batch-private-events-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/search-batch-private-events-by-ids?connectionId=$CONNECTION_ID&limit=25&offset=0&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/search-batch-private-events-by-ids?${params}`, {
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
| `requestBody` | object | yes | JSON object matching ECAL's batch events search body, for example {"ids":["event-id"]}. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": "string",
      "ecalId": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "reference": "string",
      "referenceType": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarId` | string |  |
| `ecalId` | string |  |
| `endDate` | date |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `referenceType` | string |  |
| `startDate` | date |  |
| `type` | string |  |

## Native endpoint

Through the native ECAL API, this operation is `POST /batch/events/search` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-batch-private-events-by-ids.md) for the provider-specific parameters and requirements.

