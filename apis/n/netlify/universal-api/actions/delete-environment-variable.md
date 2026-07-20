# Netlify: Delete Environment Variable



```
DELETE https://connect.mindcloud.co/v1/universal/netlify/latest/actions/delete-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/delete-environment-variable?connectionId=$CONNECTION_ID&accountId=string&key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/delete-environment-variable?${params}`, {
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
| `accountId` | string | yes |  |
| `key` | string | yes | The environment variable key (case-sensitive). |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteId` | string | no | Delete the environment variable from this site only. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |

## Native endpoint

Through the native Netlify API, this operation is `DELETE /accounts/:account_id/env/:key` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-environment-variable.md) for the provider-specific parameters and requirements.

