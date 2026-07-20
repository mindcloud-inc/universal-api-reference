# Airmeet: List Custom Registration Fields

Finds custom registration fields in an Airmeet.

```
GET https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-custom-registration-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airmeet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-custom-registration-fields?connectionId=$CONNECTION_ID&airmeetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "airmeetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airmeet/latest/actions/list-custom-registration-fields?${params}`, {
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
| `airmeetId` | string | yes | The Airmeet event ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airmeet API returns.

## Native endpoint

Through the native Airmeet API, this operation is `GET /airmeet/{airmeetId}/custom-fields` (base URL `https://api-gateway-prod.us.airmeet.com/prod`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-registration-fields.md) for the provider-specific parameters and requirements.

