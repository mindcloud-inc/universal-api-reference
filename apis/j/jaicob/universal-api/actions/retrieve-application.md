# Jaicob: Retrieve Application



```
GET https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jaicob `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-application?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaicob/latest/actions/retrieve-application?${params}`, {
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
| `id` | string | yes | Application identifier. |

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

Through the native Jaicob API, this operation is `GET /applications/public/[:id]` (base URL `https://api.jaicob.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-application.md) for the provider-specific parameters and requirements.

