# Api2Convert Universal API Examples

These examples use the MindCloud API key and Api2Convert connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Contracts

Retrieves active contract details from Api2Convert.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/get-contracts?${params}`, {
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
      "contracts": [
        {}
      ],
      "minutes_remaining": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Contracts action reference](actions/get-contracts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/api2Convert/latest/actions/get-contracts).

## Create Job

Creates a new job in Api2Convert.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "job": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/api2Convert/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "job": {}
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
      "conversion": [
        {}
      ],
      "created_at": "string",
      "errors": [
        {}
      ],
      "fail_on_conversion_error": true,
      "fail_on_input_error": true,
      "id": "string",
      "input": [
        {}
      ],
      "modified_at": "string",
      "notify_status": true,
      "output": [
        {}
      ],
      "process": true,
      "status": {},
      "token": "string",
      "type": "string",
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Job action reference](actions/create-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/api2Convert/latest/actions/create-job).
