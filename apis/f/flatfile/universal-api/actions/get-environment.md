# Flatfile: Get Environment

Retrieves a specific environment from Flatfile.

```
GET https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-environment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flatfile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-environment?connectionId=$CONNECTION_ID&environmentId=us_env_EDBDJn35" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "environmentId": "us_env_EDBDJn35"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flatfile/latest/actions/get-environment?${params}`, {
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
| `environmentId` | string | yes | Flatfile environment ID. Pass `current` to fetch the current environment. Default: `us_env_EDBDJn35`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Environment details. |

## Native endpoint

Through the native Flatfile API, this operation is `GET /environments/:environmentId` (base URL `https://api.x.flatfile.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment.md) for the provider-specific parameters and requirements.

