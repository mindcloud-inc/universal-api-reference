# Geotab: Get Asset Group



```
GET https://connect.mindcloud.co/v1/universal/geotab/latest/actions/get-asset-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geotab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geotab/latest/actions/get-asset-group?connectionId=$CONNECTION_ID&method=Get&typeName=Group&search.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "method": "Get",
  "typeName": "Group",
  "search.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geotab/latest/actions/get-asset-group?${params}`, {
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
| `method` | string | yes | Default: `Get`. |
| `typeName` | string | yes | Default: `Group`. |
| `search` | object | no |  |
| `search.id` | string | yes | The opaque MyGeotab Group ID. |
| `propertySelector` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Geotab API returns.

## Native endpoint

Through the native Geotab API, this operation is `POST` (base URL `https://{{credentials.server}}/apiv1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-group.md) for the provider-specific parameters and requirements.

