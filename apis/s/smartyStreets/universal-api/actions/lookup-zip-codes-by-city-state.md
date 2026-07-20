# Smarty-streets: Lookup ZIP Codes By City State

Finds ZIP Codes in Smarty-streets by city and state.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-zip-codes-by-city-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-zip-codes-by-city-state?connectionId=$CONNECTION_ID&city=North%20Pole&state=AK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "city": "North Pole",
  "state": "AK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/lookup-zip-codes-by-city-state?${params}`, {
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
| `city` | string | yes | City name to look up. Default: `North Pole`. Example: `North Pole`. |
| `state` | string | yes | State name or two-letter abbreviation. Default: `AK`. Example: `AK`. |

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

Through the native Smarty-streets API, this operation is `GET https://us-zipcode.api.smarty.com/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-zip-codes-by-city-state.md) for the provider-specific parameters and requirements.

