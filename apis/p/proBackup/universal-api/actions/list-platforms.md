# ProBackup: List Platforms

Retrieves active backup platforms from ProBackup.

```
GET https://connect.mindcloud.co/v1/universal/proBackup/latest/actions/list-platforms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProBackup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proBackup/latest/actions/list-platforms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proBackup/latest/actions/list-platforms?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "platforms": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `platforms` | array<object> | List of ProBackup platforms returned by the documented /backups/v1/platforms endpoint. |

## Native endpoint

Through the native ProBackup API, this operation is `GET /backups/v1/platforms` (base URL `https://api.probackup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-platforms.md) for the provider-specific parameters and requirements.

