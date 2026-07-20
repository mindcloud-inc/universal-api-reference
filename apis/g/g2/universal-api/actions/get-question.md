# G2: Get Question

Retrieves a question from G2.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-question?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/get-question?${params}`, {
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
| `id` | string | yes | Question identifier from the G2 API spec. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "description": "string",
        "inputType": "string",
        "isRequired": true,
        "questionType": "string",
        "textTemplate": "string",
        "title": "string",
        "updatedAt": "string"
      },
      "id": "string",
      "relationships": {
        "categories": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.description` | string |  |
| `attributes.inputType` | string |  |
| `attributes.isRequired` | boolean |  |
| `attributes.questionType` | string |  |
| `attributes.textTemplate` | string |  |
| `attributes.title` | string |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `relationships.categories.data[].id` | string |  |
| `relationships.categories.data[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native G2 API, this operation is `GET /api/v2/questions/:id` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

