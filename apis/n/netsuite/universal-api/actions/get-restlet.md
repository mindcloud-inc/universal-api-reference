# NetSuite - Advanced: Get Restlet



```
GET https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-restlet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Advanced `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-restlet?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-restlet?${params}`, {
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
| `script` | string | no |  |
| `deploy` | string | no |  |
| `searchId` | string | no |  |
| `expandSubResources` | boolean | no | Default: `true`. |
| `limit` | number | no |  |
| `offset` | number | no |  |
| `filter` | string | no |  |
| `sort` | string | no |  |
| `rawFilter` | string | no |  |
| `columns` | string | no |  |
| `type` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Advanced API returns.

## Native endpoint

Through the native NetSuite - Advanced API, this operation is `GET https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` (base URL `https://{{credentials.accountId}}.suitetalk.api.netsuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-restlet.md) for the provider-specific parameters and requirements.

