# PushAlert: Get Subscriber Attributes



```
GET https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-subscriber-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PushAlert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-subscriber-attributes?connectionId=$CONNECTION_ID&subscriber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushAlert/latest/actions/get-subscriber-attributes?${params}`, {
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
| `subscriber` | string | yes | Subscriber ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "msg": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Key-value attributes returned for the subscriber. |
| `msg` | string | Provider message returned when the lookup cannot be completed. |
| `success` | boolean | Whether the subscriber attribute lookup succeeded. |

## Native endpoint

Through the native PushAlert API, this operation is `POST /rest/v2/web-push/attribute/get` (base URL `https://api.pushalert.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-attributes.md) for the provider-specific parameters and requirements.

