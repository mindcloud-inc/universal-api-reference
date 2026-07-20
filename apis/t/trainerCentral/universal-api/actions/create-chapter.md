# TrainerCentral: Create Chapter

Creates a new chapter in TrainerCentral.

```
POST https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-chapter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrainerCentral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-chapter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "section.courseId": "string",
  "section.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trainerCentral/latest/actions/create-chapter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "section.courseId": "string",
    "section.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `section.courseId` | string | yes | The course ID the chapter belongs to. |
| `section.name` | string | yes | The chapter name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdTime": "string",
      "id": "string",
      "lastUpdatedBy": "string",
      "lastUpdatedTime": "string",
      "sectionId": "string",
      "sectionIndex": "string",
      "sectionName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdTime` | string |  |
| `id` | string |  |
| `lastUpdatedBy` | string |  |
| `lastUpdatedTime` | string |  |
| `sectionId` | string |  |
| `sectionIndex` | string |  |
| `sectionName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native TrainerCentral API, this operation is `POST /sections.json` (base URL `{{credentials.academyUrl}}/api/v4/{{credentials.orgId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chapter.md) for the provider-specific parameters and requirements.

