# Evalandgo: Retrieve Respondent Response

Retrieves a response for a respondent from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-respondent-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-respondent-response?connectionId=$CONNECTION_ID&respondentId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "respondentId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-respondent-response?${params}`, {
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
| `respondentId` | string | yes |  |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "id": 1,
      "personalData": {},
      "position": 1,
      "question": "string",
      "respondent": "string",
      "score": {},
      "text": "string",
      "timer": 1,
      "userEdited": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `id` | number |  |
| `personalData` | object |  |
| `position` | number |  |
| `question` | string |  |
| `respondent` | string |  |
| `score` | object |  |
| `text` | string |  |
| `timer` | number |  |
| `userEdited` | boolean |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/respondents/:respondentId/responses/:id` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-respondent-response.md) for the provider-specific parameters and requirements.

