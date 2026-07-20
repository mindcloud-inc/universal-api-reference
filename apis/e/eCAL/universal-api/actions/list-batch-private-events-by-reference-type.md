# ECAL: List Batch Private Events By Reference Type

Retrieves batch private events by ECAL reference type.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-batch-private-events-by-reference-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-batch-private-events-by-reference-type?connectionId=$CONNECTION_ID&limit=25&offset=0&referenceType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "referenceType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-batch-private-events-by-reference-type?${params}`, {
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
| `referenceType` | string | yes | Reference type used to retrieve private batch events. |

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

Through the native ECAL API, this operation is `GET /batch/events` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batch-private-events-by-reference-type.md) for the provider-specific parameters and requirements.

