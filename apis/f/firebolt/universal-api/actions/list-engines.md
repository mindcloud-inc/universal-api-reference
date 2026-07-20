# Firebolt: List Engines

Retrieves engines from Firebolt.

```
GET https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/list-engines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/list-engines?connectionId=$CONNECTION_ID&engineUrl=01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "engineUrl": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/list-engines?${params}`, {
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
| `engineUrl` | string | yes | System engine host, for example 01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io. Example: `01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-engines.md) for the provider-specific parameters and requirements.

