# Snyk: Get App By ID

Retrieves a created app from a Snyk organization.

```
GET https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-app-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Snyk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-app-by-id?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/snyk/latest/actions/get-app-by-id?${params}`, {
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
| `appId` | string | yes | Snyk app ID for the request path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "jsonapi": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `jsonapi` | object |  |
| `links` | object |  |

## Native endpoint

Through the native Snyk API, this operation is `GET /orgs/:org_id/apps/creations/:app_id` (base URL `https://api.snyk.io/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-by-id.md) for the provider-specific parameters and requirements.

