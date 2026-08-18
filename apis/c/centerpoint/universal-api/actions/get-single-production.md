# Centerpoint: Get Single Production



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-production
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-production?connectionId=$CONNECTION_ID&PRODUCTION_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "PRODUCTION_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-single-production?${params}`, {
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
| `PRODUCTION_ID` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Centerpoint API returns.

## Native endpoint

Through the native Centerpoint API, this operation is `GET productions/:PRODUCTION_ID?include=availableTransitions,availableTransitions.fromStage,availableTransitions.toStage` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-production.md) for the provider-specific parameters and requirements.

