# Clarifai: List Annotations

Retrieves annotations from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-annotations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-annotations?${params}`, {
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
| `appId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "annotations": [
        {
          "createdAt": "string",
          "data": {
            "concepts": [
              {
                "appId": "string",
                "id": "string",
                "name": "Ava Chen",
                "userId": "string",
                "value": 1
              }
            ]
          },
          "id": "string",
          "inputId": "string",
          "modifiedAt": "string",
          "status": {
            "code": 1,
            "description": "string",
            "httpStatusCode": 1
          },
          "trusted": true,
          "userId": "string",
          "worker": {
            "user": {
              "id": "string"
            }
          }
        }
      ],
      "status": {
        "code": 1,
        "description": "string",
        "httpStatusCode": 1,
        "reqId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `annotations[].createdAt` | string |  |
| `annotations[].data.concepts[].appId` | string |  |
| `annotations[].data.concepts[].id` | string |  |
| `annotations[].data.concepts[].name` | string |  |
| `annotations[].data.concepts[].userId` | string |  |
| `annotations[].data.concepts[].value` | number |  |
| `annotations[].id` | string |  |
| `annotations[].inputId` | string |  |
| `annotations[].modifiedAt` | string |  |
| `annotations[].status.code` | number |  |
| `annotations[].status.description` | string |  |
| `annotations[].status.httpStatusCode` | number |  |
| `annotations[].trusted` | boolean |  |
| `annotations[].userId` | string |  |
| `annotations[].worker.user.id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.httpStatusCode` | number |  |
| `status.reqId` | string |  |

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/annotations` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-annotations.md) for the provider-specific parameters and requirements.

