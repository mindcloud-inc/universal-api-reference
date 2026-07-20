# Formbricks: Get Response

Retrieves a response from Formbricks.

```
GET https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formbricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-response?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formbricks/latest/actions/get-response?${params}`, {
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
| `id` | string | yes | The ID of the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactAttributes": {},
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": {},
      "displayId": "string",
      "endingId": "string",
      "finished": true,
      "id": "string",
      "language": "string",
      "meta": {},
      "singleUseId": "string",
      "surveyId": "string",
      "ttc": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variables": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactAttributes` | object | Contact attributes attached to the response. |
| `contactId` | string | The ID of the contact when one is associated. |
| `createdAt` | date | The date and time the response was created. |
| `data` | object | Submitted answers keyed by question ID. |
| `displayId` | string | The display identifier for the response. |
| `endingId` | string | The ending ID when the response completed through an ending. |
| `finished` | boolean | Whether the response is finished. |
| `id` | string | The ID of the response. |
| `language` | string | The response language. |
| `meta` | object | Response metadata such as source, URL, and user agent. |
| `singleUseId` | string | The single-use link identifier when present. |
| `surveyId` | string | The ID of the survey. |
| `ttc` | object | Time-to-complete metrics by question. |
| `updatedAt` | date | The date and time the response was last updated. |
| `variables` | object | Captured survey variables. |

## Native endpoint

Through the native Formbricks API, this operation is `GET /management/responses/:id` (base URL `https://app.formbricks.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response.md) for the provider-specific parameters and requirements.

