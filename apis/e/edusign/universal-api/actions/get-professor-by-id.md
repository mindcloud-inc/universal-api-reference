# Edusign: Get Professor By ID

Retrieves a professor from Edusign by ID.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-professor-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-professor-by-id?connectionId=$CONNECTION_ID&professorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "professorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-professor-by-id?${params}`, {
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
| `professorId` | string | yes | Professor ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "apiId": "string",
        "apiType": "string",
        "dateCreated": "string",
        "dateUpdated": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "hidden": [
          "string"
        ],
        "id": "string",
        "index": 1,
        "lastname": "Chen",
        "loginCode": [
          "string"
        ],
        "magicLinkToken": "https://example.com",
        "multiAccountLoginCode": "string",
        "newPasswordToken": "string",
        "oldApiId": "string",
        "oldApiType": "string",
        "oldHidden": "string",
        "password": "string",
        "phone": "string",
        "pin": "string",
        "professorId": "string",
        "schoolDateCreated": "string",
        "schoolDateUpdated": "string",
        "schoolId": [
          "string"
        ],
        "speciality": "string",
        "tags": [
          "string"
        ],
        "teamsId": [
          "string"
        ],
        "variables": [
          {
            "dateCreated": "string",
            "dateUpdated": "string",
            "id": 1,
            "name": "Ava Chen",
            "ressourceId": "string",
            "ressourceType": "string",
            "schoolId": "string",
            "schoolVariableId": 1,
            "type": "string",
            "value": "string",
            "valueId": 1
          }
        ],
        "zoomId": [
          "string"
        ]
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.apiId` | string |  |
| `result.apiType` | string |  |
| `result.dateCreated` | string |  |
| `result.dateUpdated` | string |  |
| `result.email` | string |  |
| `result.firstname` | string |  |
| `result.hidden` | array<string> |  |
| `result.id` | string |  |
| `result.index` | number |  |
| `result.lastname` | string |  |
| `result.loginCode` | array<string> |  |
| `result.magicLinkToken` | string |  |
| `result.multiAccountLoginCode` | string |  |
| `result.newPasswordToken` | string |  |
| `result.oldApiId` | string |  |
| `result.oldApiType` | string |  |
| `result.oldHidden` | string |  |
| `result.password` | string |  |
| `result.phone` | string |  |
| `result.pin` | string |  |
| `result.professorId` | string |  |
| `result.schoolDateCreated` | string |  |
| `result.schoolDateUpdated` | string |  |
| `result.schoolId` | array<string> |  |
| `result.speciality` | string |  |
| `result.tags` | array<string> |  |
| `result.teamsId` | array<string> |  |
| `result.variables` | array<object> |  |
| `result.variables[].dateCreated` | string |  |
| `result.variables[].dateUpdated` | string |  |
| `result.variables[].id` | number |  |
| `result.variables[].name` | string |  |
| `result.variables[].ressourceId` | string |  |
| `result.variables[].ressourceType` | string |  |
| `result.variables[].schoolId` | string |  |
| `result.variables[].schoolVariableId` | number |  |
| `result.variables[].type` | string |  |
| `result.variables[].value` | string |  |
| `result.variables[].valueId` | number |  |
| `result.zoomId` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/professor/:professorId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-professor-by-id.md) for the provider-specific parameters and requirements.

