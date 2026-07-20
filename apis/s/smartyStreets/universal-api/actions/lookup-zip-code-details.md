# Smarty-streets: Lookup ZIP Code Details

Retrieves ZIP Code details from Smarty-streets.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-zip-code-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-zip-code-details?connectionId=$CONNECTION_ID&zipcode=90210" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zipcode": "90210"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-zip-code-details?${params}`, {
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
| `zipcode` | string | yes | ZIP Code to look up. Default: `90210`. Example: `90210`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cityStates": [
        {}
      ],
      "inputIndex": 1,
      "zipcodes": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cityStates` | array<object> |  |
| `inputIndex` | number |  |
| `zipcodes` | array<object> |  |

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://us-zipcode.api.smarty.com/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-zip-code-details.md) for the provider-specific parameters and requirements.

