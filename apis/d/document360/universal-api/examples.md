# Document360 Universal API Examples

These examples use the MindCloud API key and Document360 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Project Versions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-project-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-project-versions?${params}`, {
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
      "baseVersionNumber": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isBeta": true,
      "isDeprecated": true,
      "isMainVersion": true,
      "isPublic": true,
      "languageVersions": [
        {}
      ],
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "order": 1,
      "slug": "string",
      "versionCodeName": "Ava Chen",
      "versionNumber": 1,
      "versionType": 1
    }
  ],
  "meta": {}
}
```

See the full [List Project Versions action reference](actions/list-project-versions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/document360/latest/actions/list-project-versions).

## Create Article



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "projectVersionId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/document360/latest/actions/create-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "projectVersionId": "string",
    "userId": "string"
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
      "contentType": 1,
      "currentWorkflowStatusId": "string",
      "hidden": true,
      "id": "string",
      "isSharedArticle": true,
      "languageCode": "string",
      "latestVersion": 1,
      "modifiedAt": "string",
      "order": 1,
      "publicVersion": 1,
      "slug": "string",
      "status": 1,
      "title": "string",
      "translationOption": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Article action reference](actions/create-article.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/document360/latest/actions/create-article).
