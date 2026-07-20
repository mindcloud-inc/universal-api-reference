# Firebolt Universal API Examples

These examples use the MindCloud API key and Firebolt connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get System Engine URL

Retrieves a system engine URL from Firebolt.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/get-system-engine-url?connectionId=$CONNECTION_ID&accountName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/get-system-engine-url?${params}`, {
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
      "engineUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get System Engine URL action reference](actions/get-system-engine-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/firebolt/latest/actions/get-system-engine-url).

## Copy From S3

Creates a copy-from-S3 operation in Firebolt.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/copy-from-s3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "tableName": "mc_fb_copy_from_20260422",
  "source": "s3://firebolt-publishing-public/help_center_assets/firebolt_sample_dataset/levels.csv"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/copy-from-s3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
    "tableName": "mc_fb_copy_from_20260422",
    "source": "s3://firebolt-publishing-public/help_center_assets/firebolt_sample_dataset/levels.csv"
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
      "message": "string",
      "monitorSql": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy From S3 action reference](actions/copy-from-s3.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/firebolt/latest/actions/copy-from-s3).
