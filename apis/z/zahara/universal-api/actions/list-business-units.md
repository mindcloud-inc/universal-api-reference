# Zahara: List Business Units

Retrieves business units from a Zahara tenancy.

```
GET https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-business-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zahara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-business-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-business-units?${params}`, {
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
      "Archived": true,
      "BusinessUnitId": 1,
      "DateCreated": "2026-05-07T12:00:00.000Z",
      "HeadOfficeAddress": {
        "AddressId": 1,
        "AddressLines": "string",
        "AddressType": 1,
        "CountryCode": "string",
        "CountryCodeId": 1,
        "IsPrimary": true,
        "LastUpdated": "2026-05-07T12:00:00.000Z",
        "Postcode": "string",
        "Void": true
      },
      "LastUpdated": "2026-05-07T12:00:00.000Z",
      "Name": "Ava Chen",
      "Settings": {
        "DateFormat": "string",
        "DecimalPlaces": 1,
        "DefaultCurrencyId": 1,
        "Id": 1
      },
      "TenancyId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Archived` | boolean | Whether the business unit is archived. |
| `BusinessUnitId` | number | Business unit ID. |
| `DateCreated` | date | Creation timestamp. |
| `HeadOfficeAddress.AddressId` | number | Head office address ID. |
| `HeadOfficeAddress.AddressLines` | string | Head office address lines. |
| `HeadOfficeAddress.AddressType` | number | Head office address type. |
| `HeadOfficeAddress.CountryCode` | string | Head office country code. |
| `HeadOfficeAddress.CountryCodeId` | number | Head office country code ID. |
| `HeadOfficeAddress.IsPrimary` | boolean | Whether the head office address is primary. |
| `HeadOfficeAddress.LastUpdated` | date | Head office address last update timestamp. |
| `HeadOfficeAddress.Postcode` | string | Head office postcode. |
| `HeadOfficeAddress.Void` | boolean | Whether the head office address is void. |
| `LastUpdated` | date | Last update timestamp. |
| `Name` | string | Business unit name. |
| `Settings.DateFormat` | string | Configured date format. |
| `Settings.DecimalPlaces` | number | Configured decimal places. |
| `Settings.DefaultCurrencyId` | number | Default currency ID. |
| `Settings.Id` | number | Settings record ID. |
| `TenancyId` | number | Tenancy ID. |

## Native endpoint

Through the native Zahara API, this operation is `GET /api/{{credentials.tenancyApiKey}}/BusinessUnit/GetAll` (base URL `https://api.myzahara.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-business-units.md) for the provider-specific parameters and requirements.

