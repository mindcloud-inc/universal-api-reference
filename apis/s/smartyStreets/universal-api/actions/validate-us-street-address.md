# Smarty-streets: Validate US Street Address

Retrieves validated US street addresses from Smarty-streets.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-street-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-street-address?connectionId=$CONNECTION_ID&street=1%20Santa%20Claus%20Ln&city=North%20Pole&state=AK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "street": "1 Santa Claus Ln",
  "city": "North Pole",
  "state": "AK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-us-street-address?${params}`, {
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
| `street` | string | yes | Street line of the address. Default: `1 Santa Claus Ln`. |
| `city` | string | yes | City name for the address. Default: `North Pole`. |
| `state` | string | yes | State name or abbreviation. Default: `AK`. |

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

Through the native Smarty-streets API, this operation is `GET /street-address` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-us-street-address.md) for the provider-specific parameters and requirements.

