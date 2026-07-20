# SmartSuite Universal API Examples

These examples use the MindCloud API key and SmartSuite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Solutions

Retrieves solutions from SmartSuite.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-solutions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-solutions?${params}`, {
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
      "applicationsCount": 1,
      "automationCount": 1,
      "created": "string",
      "createdBy": "string",
      "deleteDate": {},
      "deletedBy": {},
      "description": {
        "data": {
          "content": [
            {
              "attrs": {
                "collapse": true,
                "id": "string",
                "indentation": {},
                "level": 1,
                "textAlign": "string"
              },
              "content": [
                {
                  "text": "string",
                  "type": "string"
                }
              ],
              "type": "string"
            }
          ],
          "type": "string"
        },
        "html": "string",
        "preview": "string"
      },
      "hasDemoData": true,
      "hidden": true,
      "homepageCategory": "string",
      "homepageCategoryName": "Ava Chen",
      "homepageCategoryOrder": {},
      "id": "string",
      "lastAccess": {},
      "logoColor": "string",
      "logoIcon": "string",
      "membersCount": 1,
      "name": "Ava Chen",
      "permissions": {
        "level": "string",
        "owners": [
          "string"
        ],
        "privateTo": "string"
      },
      "recordsCount": 1,
      "sharingAllowCopy": true,
      "sharingEnabled": true,
      "sharingHash": "string",
      "sharingPassword": "string",
      "slug": "string",
      "status": "string",
      "template": "string",
      "updated": "string",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Solutions action reference](actions/list-solutions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartSuite/latest/actions/list-solutions).

## Add Comment

Creates a new comment in SmartSuite.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "69b45da87cb40fc74dbb4b8c",
  "tableId": "69b45da87cb40fc74dbb4b84",
  "messageHtml": "<p>MC Test Comment 2</p>"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "69b45da87cb40fc74dbb4b8c",
    "tableId": "69b45da87cb40fc74dbb4b84",
    "messageHtml": "<p>MC Test Comment 2</p>"
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
      "application": "string",
      "assignedTo": {},
      "createdOn": "string",
      "deletedOn": {},
      "email": {},
      "fieldSlug": {},
      "followers": [
        "string"
      ],
      "id": "string",
      "key": 1,
      "member": "string",
      "message": {
        "data": {
          "content": [
            {
              "content": [
                {
                  "text": "string",
                  "type": "string"
                }
              ],
              "type": "string"
            }
          ],
          "type": "string"
        },
        "html": "string",
        "preview": "string"
      },
      "parentComment": {},
      "record": "string",
      "resolvedBy": {},
      "solution": "string",
      "type": "string",
      "updatedOn": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Comment action reference](actions/add-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smartSuite/latest/actions/add-comment).
