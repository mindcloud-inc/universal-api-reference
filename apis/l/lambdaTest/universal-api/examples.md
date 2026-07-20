# LambdaTest Universal API Examples

These examples use the MindCloud API key and LambdaTest connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Builds

Retrieves builds from LambdaTest.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/list-builds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/list-builds?${params}`, {
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
      "data": [
        {}
      ],
      "message": "string",
      "Meta": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Builds action reference](actions/list-builds.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lambdaTest/latest/actions/list-builds).

## Stop Build

Stops a build in LambdaTest.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/stop-build" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "buildId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/stop-build', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "buildId": "string"
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
      "data": {},
      "message": "string",
      "Meta": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Stop Build action reference](actions/stop-build.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lambdaTest/latest/actions/stop-build).
