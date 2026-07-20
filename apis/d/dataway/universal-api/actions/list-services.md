# Dataway: List Services

Retrieves available services from Dataway for a selected category.

```
GET https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dataway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-services?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataway/latest/actions/list-services?${params}`, {
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
| `slug` | string | yes | Service category slug, for example airtime or data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "billerIdentifierName": "Ava Chen",
        "name": "Ava Chen",
        "slug": "string",
        "status": "string",
        "variationLabel": "string"
      },
      "responseCode": "string",
      "responseDescription": "string",
      "responseMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of services for the selected category. |
| `data.billerIdentifierName` | string | Expected customer identifier label. |
| `data.name` | string | Service display name. |
| `data.slug` | string | Service slug. |
| `data.status` | string | Service status. |
| `data.variationLabel` | string | Label shown for variations. |
| `responseCode` | string | Provider response code. |
| `responseDescription` | string | Provider response description. |
| `responseMessage` | string | Provider response message. |

## Native endpoint

Through the native Dataway API, this operation is `GET /get-services` (base URL `https://datawayapp.com/vendor`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

