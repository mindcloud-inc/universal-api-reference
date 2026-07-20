# Tally: List Form Questions



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-form-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-form-questions?connectionId=$CONNECTION_ID&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/list-form-questions?${params}`, {
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
| `formId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "fields": [
        {
          "blockGroupUuid": "string",
          "questionType": "string",
          "title": "string",
          "type": "string",
          "uuid": "string"
        }
      ],
      "formId": "string",
      "id": "string",
      "isDeleted": true,
      "isTitleModifiedByUser": true,
      "numberOfResponses": 1,
      "title": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `fields[].blockGroupUuid` | string |  |
| `fields[].questionType` | string |  |
| `fields[].title` | string |  |
| `fields[].type` | string |  |
| `fields[].uuid` | string |  |
| `formId` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isTitleModifiedByUser` | boolean |  |
| `numberOfResponses` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET forms/:formId/questions` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-questions.md) for the provider-specific parameters and requirements.

