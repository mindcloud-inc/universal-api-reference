# Centerpoint: Get Single Property



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-property?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-property?${params}`, {
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
| `PROPERTYID` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `GET properties/:PROPERTYID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-property.md) for the provider-specific parameters and requirements.

