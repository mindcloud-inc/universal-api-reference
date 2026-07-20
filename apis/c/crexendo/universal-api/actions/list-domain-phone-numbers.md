# Crexendo: List Domain Phone Numbers

Retrieves phone numbers for a domain in Crexendo.

```
GET https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domain-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crexendo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domain-phone-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crexendo/latest/actions/list-domain-phone-numbers?${params}`, {
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
| `domain` | string | yes | Domain identifier, for example apps.mindcloud.co. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dial-rule-matching-from-uri": "string",
      "dial-rule-matching-to-uri": "string",
      "domain": "string",
      "enabled": "string",
      "phonenumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dial-rule-matching-from-uri` | string |  |
| `dial-rule-matching-to-uri` | string |  |
| `domain` | string |  |
| `enabled` | string |  |
| `phonenumber` | string |  |

## Native endpoint

Through the native Crexendo API, this operation is `GET /domains/:domain/phonenumbers` (base URL `https://ns-api.com/ns-api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domain-phone-numbers.md) for the provider-specific parameters and requirements.

