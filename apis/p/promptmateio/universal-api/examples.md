# Promptmate.io Universal API Examples

These examples use the MindCloud API key and Promptmate.io connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get App Result Rows



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/get-app-result-rows?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/get-app-result-rows?${params}`, {
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
      "appId": "string",
      "responseFields": [
        {}
      ],
      "resultData": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get App Result Rows action reference](actions/get-app-result-rows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/promptmateio/latest/actions/get-app-result-rows).

## Create App Job



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-app-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/create-app-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string",
    "data[]": [{}]
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
      "jobId": "string",
      "jobStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create App Job action reference](actions/create-app-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/promptmateio/latest/actions/create-app-job).
