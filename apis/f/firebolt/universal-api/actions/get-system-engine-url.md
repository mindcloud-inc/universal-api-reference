# Firebolt: Get System Engine URL

Retrieves a system engine URL from Firebolt.

```
GET https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/get-system-engine-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountName` | string | yes | The Firebolt account name used in the engineUrl bootstrap path. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `engineUrl` | string |  |

## Native endpoint

Through the native Firebolt API, this operation is `GET /web/v3/account/:accountName/engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-engine-url.md) for the provider-specific parameters and requirements.

