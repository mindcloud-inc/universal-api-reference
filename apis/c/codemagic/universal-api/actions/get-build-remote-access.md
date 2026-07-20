# Codemagic: Get Build Remote Access

Retrieves remote access details for a Codemagic build.

```
GET https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-remote-access
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Codemagic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-remote-access?connectionId=$CONNECTION_ID&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "buildId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-remote-access?${params}`, {
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
| `buildId` | string | yes | Codemagic build identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ssh": {},
      "vnc": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ssh` | object |  |
| `vnc` | object |  |

## Native endpoint

Through the native Codemagic API, this operation is `GET /api/v3/builds/:build_id/remote-access` (base URL `https://codemagic.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-build-remote-access.md) for the provider-specific parameters and requirements.

