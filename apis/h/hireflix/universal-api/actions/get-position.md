# Hireflix: Get Position

Retrieves a position from Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/get-position?${params}`, {
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
| `variables.id` | string | yes | The Hireflix position ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allowReviewVideoAnswers": true,
      "allowSwitchingCameras": true,
      "archived": true,
      "createdAt": 1,
      "description": "string",
      "expires": 1,
      "id": "string",
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "public": true,
      "retakes": 1,
      "timeToAnswer": 1,
      "timeToThink": 1,
      "transcriptionLanguage": "string",
      "transcriptionsSupportedLanguages": [
        "string"
      ],
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allowReviewVideoAnswers` | boolean |  |
| `allowSwitchingCameras` | boolean |  |
| `archived` | boolean |  |
| `createdAt` | number |  |
| `description` | string |  |
| `expires` | number |  |
| `id` | string |  |
| `language` | string |  |
| `location` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `public` | boolean |  |
| `retakes` | number |  |
| `timeToAnswer` | number |  |
| `timeToThink` | number |  |
| `transcriptionLanguage` | string |  |
| `transcriptionsSupportedLanguages` | array<string> |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-position.md) for the provider-specific parameters and requirements.

