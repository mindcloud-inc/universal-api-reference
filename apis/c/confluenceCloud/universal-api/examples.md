# Confluence Universal API Examples

These examples use the MindCloud API key and Confluence connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accessible Resources

Retrieves accessible Confluence sites for an OAuth app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-accessible-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/list-accessible-resources?${params}`, {
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
      "avatarUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "scopes": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Accessible Resources action reference](actions/list-accessible-resources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/confluenceCloud/latest/actions/list-accessible-resources).

## Create Attachment For Page

Creates a new attachment for a Confluence page.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/create-attachment-for-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cloudId": "string",
  "id": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/create-attachment-for-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cloudId": "string",
    "id": "string",
    "file": "string"
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
      "Links": {
        "base": "https://example.com",
        "context": "https://example.com"
      },
      "results": [
        {
          "ari": "string",
          "base64EncodedAri": "string",
          "container": {
            "ari": "string",
            "base64EncodedAri": "string",
            "Expandable": {
              "ancestors": "string",
              "body": "string",
              "children": "string",
              "childTypes": "string",
              "container": "string",
              "descendants": "string",
              "draftVersion": "string",
              "history": "string",
              "metadata": "string",
              "operations": "string",
              "restrictions": "string",
              "schedulePublishDate": "string",
              "schedulePublishInfo": "string",
              "space": "string",
              "version": "string"
            },
            "extensions": {
              "position": 1
            },
            "id": "string",
            "Links": {
              "editui": "https://example.com",
              "edituiv2": "https://example.com",
              "self": "https://example.com",
              "tinyui": "https://example.com",
              "webui": "https://example.com"
            },
            "status": "string",
            "title": "string",
            "type": "string"
          },
          "Expandable": {
            "ancestors": "string",
            "body": "string",
            "children": "string",
            "childTypes": "string",
            "descendants": "string",
            "draftVersion": "string",
            "history": "string",
            "operations": "string",
            "restrictions": "string",
            "schedulePublishDate": "string",
            "schedulePublishInfo": "string",
            "space": "string"
          },
          "extensions": {
            "collectionName": "Ava Chen",
            "comment": "string",
            "fileId": "string",
            "fileSize": 1,
            "mediaType": "string"
          },
          "id": "string",
          "Links": {
            "download": "https://example.com",
            "self": "https://example.com",
            "webui": "https://example.com"
          },
          "metadata": {
            "comment": "string",
            "Expandable": {
              "comments": "string",
              "createdBySpaceBlueprint": "string",
              "currentuser": "string",
              "frontend": "string",
              "isActiveLiveEditSession": "string",
              "lastEditedTime": "string",
              "likes": "string",
              "properties": "string",
              "simple": "string",
              "sourceTemplateEntityId": "string"
            },
            "labels": {
              "limit": 1,
              "Links": {
                "next": "https://example.com",
                "self": "https://example.com"
              },
              "size": 1,
              "start": 1
            },
            "mediaType": "string"
          },
          "status": "string",
          "title": "string",
          "type": "string",
          "version": {
            "by": {
              "accountId": "string",
              "accountStatus": "string",
              "accountType": "string",
              "displayName": "Ava Chen",
              "email": "ava@example.com",
              "Expandable": {
                "operations": "string",
                "personalSpace": "string"
              },
              "isExternalCollaborator": true,
              "isGuest": true,
              "Links": {
                "self": "https://example.com"
              },
              "locale": "string",
              "profilePicture": {
                "height": 1,
                "isDefault": true,
                "path": "string",
                "width": 1
              },
              "publicName": "Ava Chen",
              "type": "string"
            },
            "contentTypeModified": true,
            "Expandable": {
              "collaborators": "string",
              "content": "string"
            },
            "friendlyWhen": "string",
            "Links": {
              "self": "https://example.com"
            },
            "message": "string",
            "minorEdit": true,
            "number": 1,
            "when": "string"
          }
        }
      ],
      "size": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Attachment For Page action reference](actions/create-attachment-for-page.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/confluenceCloud/latest/actions/create-attachment-for-page).
