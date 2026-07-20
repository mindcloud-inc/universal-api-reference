# Cloudprinter.com: List Shipping States

Retrieves shipping states from Cloudprinter.com.

```
GET https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudprinter.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-states?connectionId=$CONNECTION_ID&countryReference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryReference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudprintercom/latest/actions/list-shipping-states?${params}`, {
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
| `countryReference` | string | yes | Country code in ISO 3166-1 alpha-2 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "note": "string",
      "state_reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `note` | string |  |
| `state_reference` | string |  |

## Native endpoint

Through the native Cloudprinter.com API, this operation is `POST /cloudcore/1.0/shipping/states` (base URL `https://api.cloudprinter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipping-states.md) for the provider-specific parameters and requirements.

