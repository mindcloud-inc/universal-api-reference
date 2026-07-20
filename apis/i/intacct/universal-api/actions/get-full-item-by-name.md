# Sage Intacct: Get Full Item By Name



```
GET https://connect.mindcloud.co/v1/universal/intacct/latest/actions/get-full-item-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sage Intacct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intacct/latest/actions/get-full-item-by-name?connectionId=$CONNECTION_ID&itemType=PROJECT&itemName=16296" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemType": "PROJECT",
  "itemName": "16296"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intacct/latest/actions/get-full-item-by-name?${params}`, {
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
| `itemType` | string | yes | Default: `PROJECT`. |
| `itemName` | string | yes | Default: `16296`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Sage Intacct API returns.

## Native endpoint

Through the native Sage Intacct API, this operation is `POST` (base URL `https://api.intacct.com/ia/xml/xmlgw.phtml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-full-item-by-name.md) for the provider-specific parameters and requirements.

