# Topia: Get Visitor Data Object

Retrieves a visitor's data object from Topia.

```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-visitor-data-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-visitor-data-object?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com&visitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com",
  "visitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-visitor-data-object?${params}`, {
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
| `urlSlug` | string | yes | Topia world URL slug. |
| `visitorId` | string | yes | Identifier for the visitor. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataObject": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataObject` | object |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/visitors/:visitorId/get-data-object` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-visitor-data-object.md) for the provider-specific parameters and requirements.

