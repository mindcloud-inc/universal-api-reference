# Unkey: Get ratelimit override

Retrieves a rate limit override from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-ratelimit-override
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-ratelimit-override?connectionId=$CONNECTION_ID&identifier=string&namespace=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "namespace": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-ratelimit-override?${params}`, {
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
| `identifier` | string | yes |  |
| `namespace` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "duration": 1,
        "identifier": "string",
        "limit": 1,
        "overrideId": "string"
      },
      "meta": {
        "requestId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.duration` | number |  |
| `data.identifier` | string |  |
| `data.limit` | number |  |
| `data.overrideId` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/ratelimit.getOverride` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ratelimit-override.md) for the provider-specific parameters and requirements.

