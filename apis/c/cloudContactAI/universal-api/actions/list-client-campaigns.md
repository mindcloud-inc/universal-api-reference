# CloudContactAI: List Client Campaigns



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-client-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-client-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/list-client-campaigns?${params}`, {
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
| `id` | string | no | The client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "client": {},
      "clientId": 1,
      "containsUrl": true,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "editable": true,
      "endDate": "2026-05-07T12:00:00.000Z",
      "errorRate": 1,
      "id": 1,
      "isDefault": true,
      "message": "string",
      "runAt": "2026-05-07T12:00:00.000Z",
      "startDate": "2026-05-07T12:00:00.000Z",
      "stats": {},
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client` | object |  |
| `clientId` | number |  |
| `containsUrl` | boolean |  |
| `createdDate` | date |  |
| `editable` | boolean |  |
| `endDate` | date |  |
| `errorRate` | number |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `message` | string |  |
| `runAt` | date |  |
| `startDate` | date |  |
| `stats` | object |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `GET api/clients/:id/campaigns` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-campaigns.md) for the provider-specific parameters and requirements.

