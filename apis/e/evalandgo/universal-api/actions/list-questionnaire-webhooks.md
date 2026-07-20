# Evalandgo: List Questionnaire Webhooks

Retrieves webhooks for a questionnaire from Evalandgo.

```
GET https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaire-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evalandgo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaire-webhooks?connectionId=$CONNECTION_ID&questionnaireId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "questionnaireId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evalandgo/latest/actions/list-questionnaire-webhooks?${params}`, {
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
| `questionnaireId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "hydra:member": [
        {
          "@id": "string",
          "@type": "string",
          "active": true,
          "createAt": "string",
          "events": [
            "string"
          ],
          "id": 1,
          "name": "Ava Chen",
          "questionnaire": "string",
          "url": "https://example.com"
        }
      ],
      "hydra:totalItems": 1
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
| `hydra:member[].@id` | string |  |
| `hydra:member[].@type` | string |  |
| `hydra:member[].active` | boolean |  |
| `hydra:member[].createAt` | string |  |
| `hydra:member[].events[]` | string |  |
| `hydra:member[].id` | number |  |
| `hydra:member[].name` | string |  |
| `hydra:member[].questionnaire` | string |  |
| `hydra:member[].url` | string |  |
| `hydra:totalItems` | number |  |

## Native endpoint

Through the native Evalandgo API, this operation is `GET /api/v3/questionnaires/:questionnaireId/webhooks` (base URL `https://app.evalandgo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questionnaire-webhooks.md) for the provider-specific parameters and requirements.

