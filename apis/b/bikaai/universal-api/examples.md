# Bika.ai Universal API Examples

These examples use the MindCloud API key and Bika.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get System Meta

Retrieves system metadata from Bika.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-system-meta?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-system-meta?${params}`, {
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
      "code": 1,
      "data": {
        "appEnv": "string",
        "buildNumber": "string",
        "buildSha": "string",
        "buildTime": "2026-05-07T12:00:00.000Z",
        "headers": {},
        "hostname": "https://example.com",
        "version": "string"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get System Meta action reference](actions/get-system-meta.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bikaai/latest/actions/get-system-meta).

## Create Database Record

Creates a database record in Bika.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/create-database-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "nodeId": "string",
  "cells": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/create-database-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "nodeId": "string",
    "cells": {}
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
      "code": 1,
      "data": {
        "cells": {},
        "commentCount": 1,
        "databaseId": "string",
        "groupCount": 1,
        "id": "string",
        "revision": 1
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Database Record action reference](actions/create-database-record.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bikaai/latest/actions/create-database-record).
