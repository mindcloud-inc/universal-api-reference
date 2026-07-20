# Sigma: List SAML Service Providers



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-saml-service-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-saml-service-providers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-saml-service-providers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | SAML service provider entries |
| `nextPageToken` | string | Cursor for the next page of service providers |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/saml/service-providers` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-saml-service-providers.md) for the provider-specific parameters and requirements.

