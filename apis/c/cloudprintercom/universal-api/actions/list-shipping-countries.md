# Cloudprinter.com: List Shipping Countries

Retrieves shipping countries from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-countries?${params}`, {
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
      "country_reference": "string",
      "note": "string",
      "require_state": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_reference` | string |  |
| `note` | string |  |
| `require_state` | number |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/shipping/countries` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipping-countries.md) for the provider-specific parameters and requirements.

