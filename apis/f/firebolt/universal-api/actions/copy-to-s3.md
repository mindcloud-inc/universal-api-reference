# Firebolt: Copy To S3

Creates a copy-to-S3 operation in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/copy-to-s3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/copy-to-s3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
  "selectQuery": "SELECT * FROM mc_fb_act_20260422_table ORDER BY id",
  "destination": "my_export_location"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/copy-to-s3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "account-1-mindcloud.api.us-east-1.app.firebolt.io",
    "selectQuery": "SELECT * FROM mc_fb_act_20260422_table ORDER BY id",
    "destination": "my_export_location"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | Firebolt user-engine host, for example account-1-mindcloud.api.us-east-1.app.firebolt.io. Example: `account-1-mindcloud.api.us-east-1.app.firebolt.io`. |
| `selectQuery` | string | yes | SELECT query whose results should be exported. Example: `SELECT * FROM mc_fb_act_20260422_table ORDER BY id`. |
| `destination` | string | yes | An Amazon S3 URL or Firebolt location object name to copy data to. Example: `my_export_location`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineName` | string | no | Optional user engine name when routing through a shared user-engine host. Example: `mc_fb_act_20260422_engine`. |
| `database` | string | no | Optional database to target for the COPY TO statement. Example: `mc_fb_act_20260422_db`. |
| `copyOptions` | string | no | Optional COPY TO options. For URL destinations that need access configuration, include the CREDENTIALS = (...) clause here. Example: `TYPE = JSON, COMPRESSION = NONE, SINGLE_FILE = TRUE, FILE_NAME_PREFIX = 'latest-export', OVERWRITE_EXISTING_FILES = TRUE`. |

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

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-to-s3.md) for the provider-specific parameters and requirements.

