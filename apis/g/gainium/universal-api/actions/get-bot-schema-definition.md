# Gainium: Get Bot Schema Definition



```
GET https://connect.mindcloud.co/v1/universal/gainium/latest/actions/get-bot-schema-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gainium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gainium/latest/actions/get-bot-schema-definition?connectionId=$CONNECTION_ID&botType=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botType": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gainium/latest/actions/get-bot-schema-definition?${params}`, {
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
| `botType` | list | yes | Bot type. One of: `0`, `1`, `2`. |
| `section` | string | no | Return only one schema section. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gainium API returns.

## Native endpoint

Through the native Gainium API, this operation is `GET /api/v2/discovery/bots/:botType` (base URL `https://api.gainium.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bot-schema-definition.md) for the provider-specific parameters and requirements.

