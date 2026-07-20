# Unkey: Get API namespace

Retrieves an API namespace from Unkey.

```
GET https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-api-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unkey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-api-namespace?connectionId=$CONNECTION_ID&apiId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unkey/latest/actions/get-api-namespace?${params}`, {
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
| `apiId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "name": "Ava Chen"
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
| `data.id` | string |  |
| `data.name` | string |  |
| `meta` | object |  |
| `meta.requestId` | string |  |

## Native endpoint

Through the native Unkey API, this operation is `POST /v2/apis.getApi` (base URL `https://api.unkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-namespace.md) for the provider-specific parameters and requirements.

