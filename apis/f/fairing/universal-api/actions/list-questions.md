# Fairing: List Questions

Retrieves questions from Fairing.

```
GET https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fairing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-questions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-questions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "allowOther": true,
      "customerType": "string",
      "frequencyType": "string",
      "id": 1,
      "insertedAt": "2026-05-07T12:00:00.000Z",
      "otherPlaceholder": "string",
      "prompt": "string",
      "publishedAt": "2026-05-07T12:00:00.000Z",
      "randomizeResponses": true,
      "responses": [
        {}
      ],
      "submitText": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowOther` | boolean | Whether customers can submit a free-form Other response. |
| `customerType` | string | Audience type targeted by the question. |
| `frequencyType` | string | How often the question is shown. |
| `id` | number | Fairing question ID. |
| `insertedAt` | date | When the question was created. |
| `otherPlaceholder` | string | Placeholder text for the Other option. |
| `prompt` | string | Question prompt shown to customers. |
| `publishedAt` | date | When the question was published. |
| `randomizeResponses` | boolean | Whether answer options are randomized. |
| `responses` | array<object> | Available answer options for the question. |
| `submitText` | string | Submit button label. |
| `type` | string | Question type. |
| `updatedAt` | date | When the question was last updated. |

## Native endpoint

Through the native Fairing API, this operation is `GET /questions` (base URL `https://app.fairing.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-questions.md) for the provider-specific parameters and requirements.

