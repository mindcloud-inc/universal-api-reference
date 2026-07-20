# Clarifai: List Concept Relations

Retrieves concept relations from Clarifai.

```
GET https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-concept-relations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-concept-relations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/list-concept-relations?${params}`, {
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
| `appId` | string | no | Clarifai app ID. |
| `conceptId` | string | no | Clarifai concept ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conceptRelations": [
        {
          "id": "string",
          "objectConcept": {
            "appId": "string",
            "createdAt": "string",
            "id": "string",
            "language": "string",
            "name": "Ava Chen",
            "userId": "string",
            "value": 1,
            "visibility": {
              "gettable": 1
            }
          },
          "predicate": "string",
          "subjectConcept": {
            "appId": "string",
            "createdAt": "string",
            "id": "string",
            "language": "string",
            "name": "Ava Chen",
            "userId": "string",
            "value": 1,
            "visibility": {
              "gettable": 1
            }
          },
          "visibility": {
            "gettable": 1
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
| `conceptRelations[].id` | string |  |
| `conceptRelations[].objectConcept.appId` | string |  |
| `conceptRelations[].objectConcept.createdAt` | string |  |
| `conceptRelations[].objectConcept.id` | string |  |
| `conceptRelations[].objectConcept.language` | string |  |
| `conceptRelations[].objectConcept.name` | string |  |
| `conceptRelations[].objectConcept.userId` | string |  |
| `conceptRelations[].objectConcept.value` | number |  |
| `conceptRelations[].objectConcept.visibility.gettable` | number |  |
| `conceptRelations[].predicate` | string |  |
| `conceptRelations[].subjectConcept.appId` | string |  |
| `conceptRelations[].subjectConcept.createdAt` | string |  |
| `conceptRelations[].subjectConcept.id` | string |  |
| `conceptRelations[].subjectConcept.language` | string |  |
| `conceptRelations[].subjectConcept.name` | string |  |
| `conceptRelations[].subjectConcept.userId` | string |  |
| `conceptRelations[].subjectConcept.value` | number |  |
| `conceptRelations[].subjectConcept.visibility.gettable` | number |  |
| `conceptRelations[].visibility.gettable` | number |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.httpStatusCode` | number |  |
| `status.reqId` | string |  |

## Native endpoint

Through the native Clarifai API, this operation is `GET /v2/users/{{credentials.userId}}/apps/{{appId}}/concepts/{{conceptId}}/relations` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-concept-relations.md) for the provider-specific parameters and requirements.

