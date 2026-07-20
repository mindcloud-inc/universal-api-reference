# mittwald: List Domain TLDs

Retrieves domain TLDs from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-domain-tlds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-domain-tlds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/list-domain-tlds?${params}`, {
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
      "irtp": true,
      "rgpDays": 1,
      "tld": "string",
      "transferAuthCodeRequired": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `irtp` | boolean |  |
| `rgpDays` | number |  |
| `tld` | string |  |
| `transferAuthCodeRequired` | boolean |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/domain-tlds` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domain-tlds.md) for the provider-specific parameters and requirements.

