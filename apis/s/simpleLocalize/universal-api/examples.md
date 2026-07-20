# SimpleLocalize Universal API Examples

These examples use the MindCloud API key and SimpleLocalize connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project Details

Retrieves project details from SimpleLocalize.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/get-project-details?${params}`, {
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
      "createdAt": "string",
      "customers": [
        {}
      ],
      "environments": [
        {}
      ],
      "hostingResources": [
        {}
      ],
      "keys": 1,
      "languages": [
        {}
      ],
      "lastActivityAt": "string",
      "lastEditedAt": "string",
      "name": "Ava Chen",
      "namespaces": [
        {}
      ],
      "projectToken": "string",
      "translatedKeysByLanguage": {},
      "translatedPercentage": 1,
      "unpublishedChanges": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Project Details action reference](actions/get-project-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleLocalize/latest/actions/get-project-details).

## Auto-Translate Text

Creates an auto-translation job for text in SimpleLocalize.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/auto-translate-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetLanguage": "string",
  "translationProvider": "DEEPL",
  "sourceText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleLocalize/latest/actions/auto-translate-text', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetLanguage": "string",
    "translationProvider": "DEEPL",
    "sourceText": "string"
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
      "translatedText": "string"
    }
  ],
  "meta": {}
}
```

See the full [Auto-Translate Text action reference](actions/auto-translate-text.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpleLocalize/latest/actions/auto-translate-text).
