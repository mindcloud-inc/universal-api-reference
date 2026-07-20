# Jaicob: List Applications



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-applications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/list-applications?${params}`, {
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
| `clientId` | string | no | Optional client filter. |
| `locationId` | string | no | Optional location filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionRequired": true,
      "applicant": {},
      "appliedWith": "string",
      "client": {},
      "coverLetter": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "rejectedExplanation": "string",
      "rejectedOn": "2026-05-07T12:00:00.000Z",
      "rejectedReason": "string",
      "remarks": "string",
      "stage": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vacancy": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionRequired` | boolean |  |
| `applicant` | object |  |
| `appliedWith` | string |  |
| `client` | object |  |
| `coverLetter` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `rejectedExplanation` | string |  |
| `rejectedOn` | date |  |
| `rejectedReason` | string |  |
| `remarks` | string |  |
| `stage` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `vacancy` | object |  |

## Native endpoint

Through the native Jaicob API, this operation is `GET /applications/public` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-applications.md) for the provider-specific parameters and requirements.

