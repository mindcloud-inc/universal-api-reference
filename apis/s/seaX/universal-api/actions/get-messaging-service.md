# SeaX: Get Messaging Service

Retrieves a messaging service from SeaX.

```
GET https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-messaging-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-messaging-service?connectionId=$CONNECTION_ID&messagingServiceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messagingServiceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seaX/latest/actions/get-messaging-service?${params}`, {
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
| `messagingServiceId` | string | yes | Messaging service identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_usecases": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "us_app_to_person_registered": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_usecases` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `phones` | array<object> |  |
| `us_app_to_person_registered` | boolean |  |

## Native endpoint

Through the native SeaX API, this operation is `GET /messaging_services/{messaging_service_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messaging-service.md) for the provider-specific parameters and requirements.

