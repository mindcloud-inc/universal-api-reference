# Connecteam Universal API Examples

These examples use the MindCloud API key and Connecteam connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/get-account-information?${params}`, {
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
      "companyId": "string",
      "companyName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Information action reference](actions/get-account-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/connecteam/latest/actions/get-account-information).

## Create Jobs

Create individual or multiple jobs under a specified scheduler

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-jobs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobs[].instanceIds[]": [
    1
  ],
  "jobs[].title": "string",
  "jobs[].subJobs[].title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/connecteam/latest/actions/create-jobs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobs[].instanceIds[]": [1],
    "jobs[].title": "string",
    "jobs[].subJobs[].title": "string"
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
      "assign": {
        "type": "string"
      },
      "code": "string",
      "color": "string",
      "description": "string",
      "gps": {
        "address": "string"
      },
      "instanceIds": [
        1
      ],
      "isDeleted": true,
      "jobId": "string",
      "subJobs": [
        {
          "assign": {
            "type": "string"
          },
          "code": "string",
          "color": "string",
          "description": "string",
          "gps": {
            "address": "string"
          },
          "isDeleted": true,
          "jobId": "string",
          "parentId": "string",
          "title": "string",
          "useParentData": true
        }
      ],
      "title": "string",
      "useParentData": true
    }
  ],
  "meta": {}
}
```

See the full [Create Jobs action reference](actions/create-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/connecteam/latest/actions/create-jobs).
