# Firebolt: Copy From S3

Creates a copy-from-S3 operation in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/copy-from-s3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `tableName` | string | yes | Target table to copy data into. Example: `mc_fb_copy_from_20260422`. |
| `source` | string | yes | An Amazon S3 URL or Firebolt location object name to copy data from. Example: `s3://firebolt-publishing-public/help_center_assets/firebolt_sample_dataset/levels.csv`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional user engine name when routing through a shared user-engine host. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional database to target for the COPY FROM statement. Example: `mc_fb_act_20260422_db`. |
| `copyOptions` | string | no | Optional COPY FROM options. For URL sources that need access configuration, include the CREDENTIALS = (...) clause here. Example: `HEADER=TRUE`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Firebolt async acceptance message. |
| `monitorSql` | string | SQL statement that can be used to check the async query status. |
| `token` | string | Firebolt async query token. |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-from-s3.md) for the provider-specific parameters and requirements.

