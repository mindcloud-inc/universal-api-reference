# Deep Infra: Get CLI Version



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-cli-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-cli-version?connectionId=$CONNECTION_ID&version=0.0.0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "version": "0.0.0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-cli-version?${params}`, {
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
| `version` | string | yes | Installed DeepInfra CLI version to check against the latest available version. Example: `0.0.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "latest": "string",
      "min": "string",
      "update": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `latest` | string | Latest available CLI version. |
| `min` | string | Minimum supported CLI version. |
| `update` | string | CLI version that should be used for update checks. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /cli/version` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cli-version.md) for the provider-specific parameters and requirements.

