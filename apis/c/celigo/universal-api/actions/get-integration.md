# Celigo: Get Integration



```
GET https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Celigo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-integration?connectionId=$CONNECTION_ID&integrationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "integrationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/celigo/latest/actions/get-integration?${params}`, {
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
| `integrationId` | list<string> | yes | Integration to get. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiGroupings": [
        "string"
      ],
      "changeEditionSteps": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "flowGroupings": [
        "string"
      ],
      "id": "string",
      "install": [
        "string"
      ],
      "installSteps": [
        {}
      ],
      "lastModified": "2026-05-07T12:00:00.000Z",
      "mode": "string",
      "name": "Ava Chen",
      "registeredConnectionIds": [
        "string"
      ],
      "sandbox": true,
      "sourceId": "string",
      "uninstallSteps": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiGroupings` | array |  |
| `changeEditionSteps` | array |  |
| `createdAt` | date |  |
| `flowGroupings` | array |  |
| `id` | string |  |
| `install` | array |  |
| `installSteps` | array<object> |  |
| `lastModified` | date |  |
| `mode` | string |  |
| `name` | string |  |
| `registeredConnectionIds` | array<string> |  |
| `sandbox` | boolean |  |
| `sourceId` | string |  |
| `uninstallSteps` | array |  |

## Native endpoint

Through the native Celigo API, this operation is `GET /integrations/:integrationId` (base URL `https://{{credentials.apiHost}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-integration.md) for the provider-specific parameters and requirements.

