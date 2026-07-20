# WaniKani: Get Study Material

Retrieves a study material from WaniKani.

```
GET https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-study-material
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-study-material?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-study-material?${params}`, {
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
| `id` | number | yes | Unique identifier of the study material. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hidden": true,
      "meaningNote": "string",
      "meaningSynonyms": [
        "string"
      ],
      "readingNote": "string",
      "subjectId": 1,
      "subjectType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `hidden` | boolean |  |
| `meaningNote` | string |  |
| `meaningSynonyms` | array<string> |  |
| `readingNote` | string |  |
| `subjectId` | number |  |
| `subjectType` | string |  |

## Native endpoint

Through the native WaniKani API, this operation is `GET /study_materials/[:id]` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-study-material.md) for the provider-specific parameters and requirements.

