# MoreApp Universal API Examples

These examples use the MindCloud API key and MoreApp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download Submission File

Downloads a submission file from MoreApp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/download-submission-file?connectionId=$CONNECTION_ID&customerId=1&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/download-submission-file?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Download Submission File action reference](actions/download-submission-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moreApp/latest/actions/download-submission-file).

## Add Form To Folder

Adds a form to a folder in MoreApp.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/add-form-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "folderId": "string",
  "formId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moreApp/latest/actions/add-form-to-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "folderId": "string",
    "formId": "string"
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
      "forms": [
        {}
      ],
      "id": "string",
      "meta": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Form To Folder action reference](actions/add-form-to-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moreApp/latest/actions/add-form-to-folder).
