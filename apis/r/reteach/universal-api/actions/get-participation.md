# Reteach: Get Participation



```
GET https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-participation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reteach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-participation?connectionId=$CONNECTION_ID&participationId=c9665f44-06c2-4490-ba9f-d3f55e1019c7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "participationId": "c9665f44-06c2-4490-ba9f-d3f55e1019c7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-participation?${params}`, {
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
| `participationId` | string | yes | The id of the participation. Default: `c9665f44-06c2-4490-ba9f-d3f55e1019c7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedCompleteConfirmationText": "string",
      "certificate": {},
      "completedAt": "string",
      "course": {},
      "customer": {},
      "deadline": "string",
      "externalId": "string",
      "id": "string",
      "invitationAcceptedAt": "string",
      "invitedAt": "string",
      "isRequired": true,
      "joinedAt": "string",
      "progress": 1,
      "startedAt": "string",
      "status": "string",
      "timeSpentToComplete": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedCompleteConfirmationText` | string |  |
| `certificate` | object |  |
| `completedAt` | string |  |
| `course` | object |  |
| `customer` | object |  |
| `deadline` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `invitationAcceptedAt` | string |  |
| `invitedAt` | string |  |
| `isRequired` | boolean |  |
| `joinedAt` | string |  |
| `progress` | number |  |
| `startedAt` | string |  |
| `status` | string |  |
| `timeSpentToComplete` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Reteach API, this operation is `GET /participation/{participationId}` (base URL `https://api.reteach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-participation.md) for the provider-specific parameters and requirements.

