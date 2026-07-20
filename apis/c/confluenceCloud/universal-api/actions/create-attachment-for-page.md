# Confluence: Create Attachment For Page

Creates a new attachment for a Confluence page.

```
POST https://connect.mindcloud.co/v1/universal/confluenceCloud/latest/actions/create-attachment-for-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Confluence `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cloudId` | string | yes | Confluence cloud ID for the target site. |
| `id` | string | yes | Confluence page ID to attach the file to. |
| `file` | file | yes | File content to upload as the attachment. |
| `comment` | string | no | Optional attachment comment. |
| `minorEdit` | boolean | no | Whether the upload should be marked as a minor edit. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Links.base` | string |  |
| `Links.context` | string |  |
| `results[].ari` | string |  |
| `results[].base64EncodedAri` | string |  |
| `results[].container.ari` | string |  |
| `results[].container.base64EncodedAri` | string |  |
| `results[].container.Expandable.ancestors` | string |  |
| `results[].container.Expandable.body` | string |  |
| `results[].container.Expandable.children` | string |  |
| `results[].container.Expandable.childTypes` | string |  |
| `results[].container.Expandable.container` | string |  |
| `results[].container.Expandable.descendants` | string |  |
| `results[].container.Expandable.draftVersion` | string |  |
| `results[].container.Expandable.history` | string |  |
| `results[].container.Expandable.metadata` | string |  |
| `results[].container.Expandable.operations` | string |  |
| `results[].container.Expandable.restrictions` | string |  |
| `results[].container.Expandable.schedulePublishDate` | string |  |
| `results[].container.Expandable.schedulePublishInfo` | string |  |
| `results[].container.Expandable.space` | string |  |
| `results[].container.Expandable.version` | string |  |
| `results[].container.extensions.position` | number |  |
| `results[].container.id` | string |  |
| `results[].container.Links.editui` | string |  |
| `results[].container.Links.edituiv2` | string |  |
| `results[].container.Links.self` | string |  |
| `results[].container.Links.tinyui` | string |  |
| `results[].container.Links.webui` | string |  |
| `results[].container.status` | string |  |
| `results[].container.title` | string |  |
| `results[].container.type` | string |  |
| `results[].Expandable.ancestors` | string |  |
| `results[].Expandable.body` | string |  |
| `results[].Expandable.children` | string |  |
| `results[].Expandable.childTypes` | string |  |
| `results[].Expandable.descendants` | string |  |
| `results[].Expandable.draftVersion` | string |  |
| `results[].Expandable.history` | string |  |
| `results[].Expandable.operations` | string |  |
| `results[].Expandable.restrictions` | string |  |
| `results[].Expandable.schedulePublishDate` | string |  |
| `results[].Expandable.schedulePublishInfo` | string |  |
| `results[].Expandable.space` | string |  |
| `results[].extensions.collectionName` | string |  |
| `results[].extensions.comment` | string |  |
| `results[].extensions.fileId` | string |  |
| `results[].extensions.fileSize` | number |  |
| `results[].extensions.mediaType` | string |  |
| `results[].id` | string |  |
| `results[].Links.download` | string |  |
| `results[].Links.self` | string |  |
| `results[].Links.webui` | string |  |
| `results[].metadata.comment` | string |  |
| `results[].metadata.Expandable.comments` | string |  |
| `results[].metadata.Expandable.createdBySpaceBlueprint` | string |  |
| `results[].metadata.Expandable.currentuser` | string |  |
| `results[].metadata.Expandable.frontend` | string |  |
| `results[].metadata.Expandable.isActiveLiveEditSession` | string |  |
| `results[].metadata.Expandable.lastEditedTime` | string |  |
| `results[].metadata.Expandable.likes` | string |  |
| `results[].metadata.Expandable.properties` | string |  |
| `results[].metadata.Expandable.simple` | string |  |
| `results[].metadata.Expandable.sourceTemplateEntityId` | string |  |
| `results[].metadata.labels.limit` | number |  |
| `results[].metadata.labels.Links.next` | string |  |
| `results[].metadata.labels.Links.self` | string |  |
| `results[].metadata.labels.size` | number |  |
| `results[].metadata.labels.start` | number |  |
| `results[].metadata.mediaType` | string |  |
| `results[].status` | string |  |
| `results[].title` | string |  |
| `results[].type` | string |  |
| `results[].version.by.accountId` | string |  |
| `results[].version.by.accountStatus` | string |  |
| `results[].version.by.accountType` | string |  |
| `results[].version.by.displayName` | string |  |
| `results[].version.by.email` | string |  |
| `results[].version.by.Expandable.operations` | string |  |
| `results[].version.by.Expandable.personalSpace` | string |  |
| `results[].version.by.isExternalCollaborator` | boolean |  |
| `results[].version.by.isGuest` | boolean |  |
| `results[].version.by.Links.self` | string |  |
| `results[].version.by.locale` | string |  |
| `results[].version.by.profilePicture.height` | number |  |
| `results[].version.by.profilePicture.isDefault` | boolean |  |
| `results[].version.by.profilePicture.path` | string |  |
| `results[].version.by.profilePicture.width` | number |  |
| `results[].version.by.publicName` | string |  |
| `results[].version.by.type` | string |  |
| `results[].version.contentTypeModified` | boolean |  |
| `results[].version.Expandable.collaborators` | string |  |
| `results[].version.Expandable.content` | string |  |
| `results[].version.friendlyWhen` | string |  |
| `results[].version.Links.self` | string |  |
| `results[].version.message` | string |  |
| `results[].version.minorEdit` | boolean |  |
| `results[].version.number` | number |  |
| `results[].version.when` | string |  |
| `size` | number |  |

## Native endpoint

Through the native Confluence API, this operation is `POST /ex/confluence/:cloudId/wiki/rest/api/content/:id/child/attachment` (base URL `https://api.atlassian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-attachment-for-page.md) for the provider-specific parameters and requirements.

