# Ideal Postcodes: Verify Address

Verifies and standardizes a US address in Ideal Postcodes.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/verify-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/verify-address?connectionId=$CONNECTION_ID&query=123%20Main%20St%2C%20Springfield%2C%20IL%2062701" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "123 Main St, Springfield, IL 62701"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/verify-address?${params}`, {
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
| `query` | string | yes | Address input to verify. Default: `123 Main St, Springfield, IL 62701`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `zipCode` | string | no | ZIP code for the address. |
| `city` | string | no | City component for the address. |
| `state` | string | no | State abbreviation for the address. |
| `context` | string | no | Country context to use when verifying the address, for example USA. |
| `tags` | string | no | Comma-separated tags used to annotate the request context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressLineOne": "string",
      "addressLineTwo": "string",
      "city": "string",
      "confidence": 1,
      "count": 1,
      "countryIso2": "string",
      "fit": 1,
      "match": {
        "address1": "string",
        "address2": "string",
        "address3": "string",
        "areaCode": "string",
        "carrierRoute": "string",
        "checkDigit": "string",
        "city": "string",
        "cityAbbreviation": "string",
        "congressionalDistrict": "string",
        "countryCode": "string",
        "county": "string",
        "dayLightSavings": true,
        "deliveryPoint": "string",
        "dpv": "string",
        "dpvCmra": "string",
        "dpvFootnotes": "string",
        "dpvNoStat": "string",
        "dpvVacant": "string",
        "elot": "string",
        "financeNumber": "string",
        "fipsCountyCode": "string",
        "firm": "string",
        "footnotes": "string",
        "geoCoded": true,
        "lacsIndicator": "string",
        "lacsLinkFootnote": "https://example.com",
        "lacsLinkIndicator": "https://example.com",
        "latitude": "string",
        "longitude": "string",
        "parsedPmbDesignator": "string",
        "parsedPmbNumber": "string",
        "parsedPostDirectional": "string",
        "parsedPreDirectional": "string",
        "parsedPrimaryNumber": "string",
        "parsedStreetName": "Ava Chen",
        "parsedSuffix": "string",
        "parsedUnitDesignator": "string",
        "parsedUnitNumber": "string",
        "rdi": "string",
        "recordType": "string",
        "state": "string",
        "suiteLinkFootnote": "https://example.com",
        "timeZone": "string",
        "urbanization": "string",
        "zipCode": "string"
      },
      "matchInformation": "string",
      "query": "string",
      "queryCity": "string",
      "queryState": "string",
      "queryZipCode": "string",
      "state": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLineOne` | string |  |
| `addressLineTwo` | string |  |
| `city` | string |  |
| `confidence` | number |  |
| `count` | number |  |
| `countryIso2` | string |  |
| `fit` | number |  |
| `match.address1` | string |  |
| `match.address2` | string |  |
| `match.address3` | string |  |
| `match.areaCode` | string |  |
| `match.carrierRoute` | string |  |
| `match.checkDigit` | string |  |
| `match.city` | string |  |
| `match.cityAbbreviation` | string |  |
| `match.congressionalDistrict` | string |  |
| `match.countryCode` | string |  |
| `match.county` | string |  |
| `match.dayLightSavings` | boolean |  |
| `match.deliveryPoint` | string |  |
| `match.dpv` | string |  |
| `match.dpvCmra` | string |  |
| `match.dpvFootnotes` | string |  |
| `match.dpvNoStat` | string |  |
| `match.dpvVacant` | string |  |
| `match.elot` | string |  |
| `match.financeNumber` | string |  |
| `match.fipsCountyCode` | string |  |
| `match.firm` | string |  |
| `match.footnotes` | string |  |
| `match.geoCoded` | boolean |  |
| `match.lacsIndicator` | string |  |
| `match.lacsLinkFootnote` | string |  |
| `match.lacsLinkIndicator` | string |  |
| `match.latitude` | string |  |
| `match.longitude` | string |  |
| `match.parsedPmbDesignator` | string |  |
| `match.parsedPmbNumber` | string |  |
| `match.parsedPostDirectional` | string |  |
| `match.parsedPreDirectional` | string |  |
| `match.parsedPrimaryNumber` | string |  |
| `match.parsedStreetName` | string |  |
| `match.parsedSuffix` | string |  |
| `match.parsedUnitDesignator` | string |  |
| `match.parsedUnitNumber` | string |  |
| `match.rdi` | string |  |
| `match.recordType` | string |  |
| `match.state` | string |  |
| `match.suiteLinkFootnote` | string |  |
| `match.timeZone` | string |  |
| `match.urbanization` | string |  |
| `match.zipCode` | string |  |
| `matchInformation` | string |  |
| `query` | string |  |
| `queryCity` | string |  |
| `queryState` | string |  |
| `queryZipCode` | string |  |
| `state` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `POST /verify/addresses` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-address.md) for the provider-specific parameters and requirements.

