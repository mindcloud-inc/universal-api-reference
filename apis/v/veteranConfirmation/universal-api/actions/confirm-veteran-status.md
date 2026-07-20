# Veteran Confirmation: Confirm Veteran Status



```
GET https://connect.mindcloud.co/v1/universal/veteranConfirmation/latest/actions/confirm-veteran-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veteran Confirmation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veteranConfirmation/latest/actions/confirm-veteran-status?connectionId=$CONNECTION_ID&firstName=Alfredo&lastName=Armstrong&birthDate=1993-06-08&streetAddressLine1=17020%20Tortoise%20St&city=Round%20Rock&state=TX&zipCode=78664&country=USA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "Alfredo",
  "lastName": "Armstrong",
  "birthDate": "1993-06-08",
  "streetAddressLine1": "17020 Tortoise St",
  "city": "Round Rock",
  "state": "TX",
  "zipCode": "78664",
  "country": "USA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veteranConfirmation/latest/actions/confirm-veteran-status?${params}`, {
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
| `firstName` | string | yes | Person's first name. Default: `Alfredo`. |
| `middleName` | string | no | Person's middle name. Default: `M`. |
| `lastName` | string | yes | Person's last name. Default: `Armstrong`. |
| `birthDate` | date | yes | Birth date in YYYY-MM-DD format. Default: `1993-06-08`. |
| `gender` | string | no | Gender value; only M or F helps the search currently. Default: `M`. |
| `streetAddressLine1` | string | yes | Current residence street address line 1. Default: `17020 Tortoise St`. |
| `city` | string | yes | Current residence city. Default: `Round Rock`. |
| `state` | string | yes | Current residence state. Default: `TX`. |
| `zipCode` | string | yes | Current residence zip code. Default: `78664`. |
| `country` | string | yes | Current residence country. Default: `USA`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `streetAddressLine2` | string | no | Current residence street address line 2. |
| `streetAddressLine3` | string | no | Current residence street address line 3. |
| `homePhoneNumber` | string | no | Home phone number. Default: `555-555-5555`. |
| `mothersMaidenName` | string | no | Mother's maiden name. Default: `Smith`. |
| `birthPlaceCity` | string | no | Birth place city. Default: `Johnson City`. |
| `birthPlaceState` | string | no | Birth place state. Default: `MA`. |
| `birthPlaceCountry` | string | no | Birth place country. Default: `USA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": {},
      "notConfirmedReason": "string",
      "veteranStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | object |  |
| `notConfirmedReason` | string |  |
| `veteranStatus` | string |  |

## Native endpoint

Through the native Veteran Confirmation API, this operation is `POST /status` (base URL `https://sandbox-api.va.gov/services/veteran-confirmation/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-veteran-status.md) for the provider-specific parameters and requirements.

