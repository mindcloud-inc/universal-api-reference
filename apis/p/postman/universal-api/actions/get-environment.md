# Postman: Get Environment

Retrieves details for an environment from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-environment?connectionId=$CONNECTION_ID&environmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-environment?${params}`, {
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
| `environmentId` | string | yes | The environment's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environment": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "isPublic": true,
        "name": "Ava Chen",
        "uid": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environment.createdAt` | date |  |
| `environment.id` | string |  |
| `environment.isPublic` | boolean |  |
| `environment.name` | string |  |
| `environment.uid` | string |  |
| `environment.updatedAt` | date |  |

## Native endpoint

Through the native Postman API, this operation is `GET /environments/:environmentId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment.md) for the provider-specific parameters and requirements.

