# Evalandgo: Retrieve Form Response

Retrieves a form response from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-form-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-form-response?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/retrieve-form-response?${params}`, {
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
      "responseInputs": [
        {
          "@id": "string",
          "@type": "string",
          "input": "string",
          "response": "string",
          "text": "string"
        }
      ],
      "score": {},
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
| `responseInputs[].@id` | string |  |
| `responseInputs[].@type` | string |  |
| `responseInputs[].input` | string |  |
| `responseInputs[].response` | string |  |
| `responseInputs[].text` | string |  |
| `score` | object |  |
| `timer` | number |  |
| `userEdited` | boolean |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/responses/form/:id` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form-response.md) for the provider-specific parameters and requirements.

