# Smarty-streets: Validate US Address With IANA Timezone

Retrieves US address validation details from Smarty-streets with IANA timezone data.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-address-with-iana-timezone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-address-with-iana-timezone?connectionId=$CONNECTION_ID&street=1%20Santa%20Claus%20Ln%2C%20North%20Pole%2C%20AK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "street": "1 Santa Claus Ln, North Pole, AK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-address-with-iana-timezone?${params}`, {
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
| `street` | string | yes | Address text to verify. Default: `1 Santa Claus Ln, North Pole, AK`. Example: `1 Santa Claus Ln, North Pole, AK`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analysis": {},
      "candidateIndex": 1,
      "components": {},
      "deliveryLine1": "string",
      "inputIndex": 1,
      "lastLine": "string",
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analysis` | object |  |
| `candidateIndex` | number |  |
| `components` | object |  |
| `deliveryLine1` | string |  |
| `inputIndex` | number |  |
| `lastLine` | string |  |
| `metadata` | object |  |

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://us-street.api.smarty.com/street-address` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-us-address-with-iana-timezone.md) for the provider-specific parameters and requirements.

