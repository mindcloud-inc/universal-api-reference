# Stigg: List Customer Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/stigg/latest/actions/list-customer-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stigg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stigg/latest/actions/list-customer-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stigg/latest/actions/list-customer-subscriptions?${params}`, {
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
| `query` | string | no | GraphQL query document to execute for this Stigg operation. |
| `variables` | string | no | GraphQL variables object for this Stigg operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "refId": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `items` | array<object> |  |
| `message` | string |  |
| `refId` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Stigg API, this operation is `POST /graphql` (base URL `https://api.stigg.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-subscriptions.md) for the provider-specific parameters and requirements.

