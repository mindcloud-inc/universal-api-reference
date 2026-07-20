# Filestack Universal API Examples

These examples use the MindCloud API key and Filestack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get File Metadata

Retrieves file metadata from Filestack.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestack/latest/actions/get-file-metadata?connectionId=$CONNECTION_ID&handle=DCL5K46FS3OIxb5iuKby" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "DCL5K46FS3OIxb5iuKby"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestack/latest/actions/get-file-metadata?${params}`, {
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
      "filename": "Ava Chen",
      "mimetype": "string",
      "size": 1,
      "uploaded": 1,
      "writeable": true
    }
  ],
  "meta": {}
}
```

See the full [Get File Metadata action reference](actions/get-file-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/filestack/latest/actions/get-file-metadata).

## Run Workflow On File

Runs a workflow on a file in Filestack.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestack/latest/actions/run-workflow-on-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "67d273c3-249c-4192-b228-9c3e1d003963",
  "handle": "pR4oeS63QLmYIFNs2ZvZ",
  "policy": "eyJleHBpcnkiOjE3MDAwMDAwMDB9",
  "signature": "428c3b32063f2081ec1ee3a703d05ce19883849adb4c90224367fe9707b3d808"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestack/latest/actions/run-workflow-on-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "67d273c3-249c-4192-b228-9c3e1d003963",
    "handle": "pR4oeS63QLmYIFNs2ZvZ",
    "policy": "eyJleHBpcnkiOjE3MDAwMDAwMDB9",
    "signature": "428c3b32063f2081ec1ee3a703d05ce19883849adb4c90224367fe9707b3d808"
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
      "jobid": "string",
      "sources": [
        "string"
      ],
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflow": "string"
    }
  ],
  "meta": {}
}
```

See the full [Run Workflow On File action reference](actions/run-workflow-on-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/filestack/latest/actions/run-workflow-on-file).
