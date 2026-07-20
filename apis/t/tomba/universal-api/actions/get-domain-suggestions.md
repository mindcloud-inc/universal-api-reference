# Tomba: Get Domain Suggestions

Finds domain suggestions in Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-domain-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-domain-suggestions?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-domain-suggestions?${params}`, {
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
| `query` | string | yes | Company name or domain to find related suggestions for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "domain": "string",
          "email_count": 1,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].domain` | string |  |
| `[].email_count` | number |  |
| `[].name` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /domain-suggestions` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-suggestions.md) for the provider-specific parameters and requirements.

