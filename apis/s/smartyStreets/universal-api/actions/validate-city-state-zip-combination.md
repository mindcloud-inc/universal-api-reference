# Smarty-streets: Validate City State ZIP Combination

Retrieves validation details for a city, state, and ZIP combination in Smarty-streets.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-city-state-zip-combination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-city-state-zip-combination?connectionId=$CONNECTION_ID&city=Mountain%20View&state=CA&zipcode=94035" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "city": "Mountain View",
  "state": "CA",
  "zipcode": "94035"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/validate-city-state-zip-combination?${params}`, {
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
| `city` | string | yes | City name to validate. Default: `Mountain View`. Example: `Mountain View`. |
| `state` | string | yes | State name or two-letter abbreviation. Default: `CA`. Example: `CA`. |
| `zipcode` | string | yes | ZIP Code to validate with the city and state. Default: `94035`. Example: `94035`. |

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

Through the native Smarty-streets API, this operation is `GET https://us-zipcode.api.smarty.com/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-city-state-zip-combination.md) for the provider-specific parameters and requirements.

