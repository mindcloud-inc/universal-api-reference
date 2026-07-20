# Smartcat: Get Translation Memory

Retrieves translation memory details from Smartcat.

```
GET https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-translation-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-translation-memory?connectionId=$CONNECTION_ID&tmId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tmId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/get-translation-memory?${params}`, {
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
| `tmId` | string | yes | Smartcat translation memory ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isAutomaticallyCreated": true,
      "name": "Ava Chen",
      "sourceLanguage": "string",
      "targetLanguages": [
        "string"
      ],
      "unitCountByLanguageId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Owning Smartcat account ID |
| `createdDate` | date | Translation memory creation timestamp |
| `description` | string | Translation memory description |
| `id` | string | Translation memory ID |
| `isAutomaticallyCreated` | boolean | Whether Smartcat created the TM automatically |
| `name` | string | Translation memory name |
| `sourceLanguage` | string | Source language code |
| `targetLanguages` | array<string> | Configured target language codes |
| `unitCountByLanguageId` | object | Unit counts by target language identifier |

## Native endpoint

Through the native Smartcat API, this operation is `GET /api/integration/v1/translationmemory/:tmId` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-translation-memory.md) for the provider-specific parameters and requirements.

