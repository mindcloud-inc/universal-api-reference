# WaniKani Universal API Examples

These examples use the MindCloud API key and WaniKani connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Information

Retrieves user information from WaniKani.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/get-user-information?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "currentVacationStartedAt": {},
      "id": "string",
      "level": 1,
      "preferences": {
        "defaultVoiceActorId": 1,
        "extraStudyAutoplayAudio": true,
        "lessonsAutoplayAudio": true,
        "lessonsBatchSize": 1,
        "lessonsPresentationOrder": "string",
        "reviewsAutoplayAudio": true,
        "reviewsDisplaySrsIndicator": true,
        "reviewsPresentationOrder": "string"
      },
      "profileUrl": "https://example.com",
      "startedAt": "string",
      "subscription": {
        "active": true,
        "maxLevelGranted": 1,
        "periodEndsAt": {},
        "type": "string"
      },
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User Information action reference](actions/get-user-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waniKani/latest/actions/get-user-information).

## Create Study Material

Creates a new study material in WaniKani.

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

Example response:

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

See the full [Create Study Material action reference](actions/create-study-material.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waniKani/latest/actions/create-study-material).
