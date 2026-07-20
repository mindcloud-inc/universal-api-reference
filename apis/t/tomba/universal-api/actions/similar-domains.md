# Tomba: Similar Domains

Finds similar domains in Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/similar-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/similar-domains?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/similar-domains?${params}`, {
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
| `domain` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "industries": "string",
          "name": "Ava Chen",
          "website_url": "https://example.com"
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
| `[].industries` | string |  |
| `[].name` | string |  |
| `[].website_url` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /similar` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/similar-domains.md) for the provider-specific parameters and requirements.

