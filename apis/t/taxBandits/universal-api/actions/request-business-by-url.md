# TaxBandits: Request Business by URL

Retrieves a business request URL from TaxBandits.

```
GET https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/request-business-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaxBandits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/request-business-by-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taxBandits/latest/actions/request-business-by-url?${params}`, {
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
| `cancelUrl` | string | no | Redirect URL after cancel. |
| `formType` | string | no | Target form type for the business request URL. |
| `payerRef` | string | no | Payer reference used to generate the business URL. |
| `returnUrl` | string | no | Redirect URL after successful completion. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessUrl": "https://example.com",
      "Errors": [
        {}
      ],
      "PayerRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessUrl` | string |  |
| `Errors` | array<object> |  |
| `PayerRef` | string |  |

## Native endpoint

Through the native TaxBandits API, this operation is `GET Business/RequestByURL` (base URL `https://testapi.taxbandits.com/v1.7.3/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-business-by-url.md) for the provider-specific parameters and requirements.

