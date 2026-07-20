# Myphoner: Get Call Information

Retrieves details for a call from Myphoner.

```
GET https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/get-call-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/get-call-information?connectionId=$CONNECTION_ID&callId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/get-call-information?${params}`, {
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
| `callId` | number | yes | The Myphoner call ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destinationNumber": "string",
      "duration": 1,
      "location": "string",
      "recordings": [
        {
          "startedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ],
      "startedAt": "2026-05-07T12:00:00.000Z",
      "userEmail": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destinationNumber` | string |  |
| `duration` | number |  |
| `location` | string |  |
| `recordings` | array<object> |  |
| `recordings[].startedAt` | date |  |
| `recordings[].url` | string |  |
| `startedAt` | date |  |
| `userEmail` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `GET /calls/:callId` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-information.md) for the provider-specific parameters and requirements.

