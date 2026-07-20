# Clarifai: Update Annotations

Updates existing annotations in Clarifai.

```
PATCH https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PATCH "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-annotations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/update-annotations', {
  method: 'PATCH',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Clarifai API, this operation is `PATCH /v2/annotations` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-annotations.md) for the provider-specific parameters and requirements.

