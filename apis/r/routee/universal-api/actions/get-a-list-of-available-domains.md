# Routee: Get a list of available domains

Retrieves a list of available domains from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-a-list-of-available-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-a-list-of-available-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/get-a-list-of-available-domains?${params}`, {
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
| `domains[]` | array<object> | no | Array of the domain object |
| `name` | string | no | The domain name |
| `available` | boolean | no | Whether the domain is available for use or not. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domains": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domains[]` | array<object> |  |
| `domains[].available` | boolean |  |
| `domains[].name` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /shorten/domains` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-list-of-available-domains.md) for the provider-specific parameters and requirements.

