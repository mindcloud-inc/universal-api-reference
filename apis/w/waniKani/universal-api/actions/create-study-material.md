# WaniKani: Create Study Material

Creates a new study material in WaniKani.

```
POST https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/create-study-material
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/create-study-material" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "study_material.subject_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/create-study-material', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "study_material.subject_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `study_material.subject_id` | number | yes | Unique identifier of the subject. |
| `study_material.meaning_note` | string | no | Meaning notes specific for the subject. |

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

Through the native WaniKani API, this operation is `POST /study_materials` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-study-material.md) for the provider-specific parameters and requirements.

