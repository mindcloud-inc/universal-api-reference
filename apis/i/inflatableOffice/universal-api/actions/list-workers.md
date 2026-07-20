# InflatableOffice: List Workers

Retrieves workers from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-workers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-workers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-workers?${params}`, {
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
| `body` | boolean | no | When true, returns more worker details. |
| `approved` | boolean | no | When true, returns only approved workers. |
| `vehicle` | boolean | no | When true, returns vehicles instead of workers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "addressgeolocation": "string",
      "allowunsavedchanges": "string",
      "approved": "string",
      "attempts": "string",
      "betauser": "string",
      "calendlyuserlink": "https://example.com",
      "carrier": "string",
      "cashappusername": "Ava Chen",
      "city": "string",
      "color": "string",
      "colorblind": "string",
      "commissionCouponspackages": "string",
      "commissionDeliveryfees": "string",
      "commissionDiscounts": "string",
      "commissionFees": "string",
      "commissionPercentage": "string",
      "commissionRentalsubtotal": "string",
      "commissionSalestax": "string",
      "commissionSpecials": "string",
      "commissionStaffcosts": "string",
      "country": "string",
      "cphone": "string",
      "darkmode": "string",
      "dateformat": "string",
      "dayofweek": "string",
      "defaulthomepage": "string",
      "defaultlocation": "string",
      "defaultphone": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "gcalendarid": "string",
      "gcalfailures": "string",
      "gmailtoken": "string",
      "hideshifts": "string",
      "hideunselecteditems": "string",
      "hphone": "string",
      "href": "string",
      "id": "string",
      "inventoryexportid": "string",
      "inventoryfilterid": "string",
      "iocid": "string",
      "isquickbooks": "string",
      "jiraid": "string",
      "language": "string",
      "lastattempttime": "string",
      "lastname": "Chen",
      "lastvisit": "string",
      "lastvisitTs": "string",
      "lastvisitUtc": "string",
      "lattitude": "string",
      "leadexporttid": "string",
      "leadhoverdefault": "string",
      "leadmoddays": "string",
      "leadrentalconcise": "string",
      "longitude": "string",
      "mileagerate": "string",
      "mileagestart": "string",
      "modifiedtime": "string",
      "modifiedtimeTs": {},
      "modifiedtimeUtc": "string",
      "mpg": "string",
      "notes": "string",
      "ophone": "string",
      "outlookexpires": "string",
      "outlookrefreshtoken": "string",
      "outlooktoken": "string",
      "overviewfilter": "string",
      "paypalusername": "Ava Chen",
      "payrate": "string",
      "profileimage": "string",
      "rank": "string",
      "regtime": "string",
      "regtimeTs": "string",
      "regtimeUtc": "string",
      "state": "string",
      "supervisorid": "string",
      "timeformat": "string",
      "usemfa": "string",
      "venmousername": "Ava Chen",
      "weightcapacity": "string",
      "wordpressapi": "string",
      "wuname": "Ava Chen",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `addressgeolocation` | string |  |
| `allowunsavedchanges` | string |  |
| `approved` | string |  |
| `attempts` | string |  |
| `betauser` | string |  |
| `calendlyuserlink` | string |  |
| `carrier` | string |  |
| `cashappusername` | string |  |
| `city` | string |  |
| `color` | string |  |
| `colorblind` | string |  |
| `commissionCouponspackages` | string |  |
| `commissionDeliveryfees` | string |  |
| `commissionDiscounts` | string |  |
| `commissionFees` | string |  |
| `commissionPercentage` | string |  |
| `commissionRentalsubtotal` | string |  |
| `commissionSalestax` | string |  |
| `commissionSpecials` | string |  |
| `commissionStaffcosts` | string |  |
| `country` | string |  |
| `cphone` | string |  |
| `darkmode` | string |  |
| `dateformat` | string |  |
| `dayofweek` | string |  |
| `defaulthomepage` | string |  |
| `defaultlocation` | string |  |
| `defaultphone` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `gcalendarid` | string |  |
| `gcalfailures` | string |  |
| `gmailtoken` | string |  |
| `hideshifts` | string |  |
| `hideunselecteditems` | string |  |
| `hphone` | string |  |
| `href` | string |  |
| `id` | string |  |
| `inventoryexportid` | string |  |
| `inventoryfilterid` | string |  |
| `iocid` | string |  |
| `isquickbooks` | string |  |
| `jiraid` | string |  |
| `language` | string |  |
| `lastattempttime` | string |  |
| `lastname` | string |  |
| `lastvisit` | string |  |
| `lastvisitTs` | string |  |
| `lastvisitUtc` | string |  |
| `lattitude` | string |  |
| `leadexporttid` | string |  |
| `leadhoverdefault` | string |  |
| `leadmoddays` | string |  |
| `leadrentalconcise` | string |  |
| `longitude` | string |  |
| `mileagerate` | string |  |
| `mileagestart` | string |  |
| `modifiedtime` | string |  |
| `modifiedtimeTs` | object |  |
| `modifiedtimeUtc` | string |  |
| `mpg` | string |  |
| `notes` | string |  |
| `ophone` | string |  |
| `outlookexpires` | string |  |
| `outlookrefreshtoken` | string |  |
| `outlooktoken` | string |  |
| `overviewfilter` | string |  |
| `paypalusername` | string |  |
| `payrate` | string |  |
| `profileimage` | string |  |
| `rank` | string |  |
| `regtime` | string |  |
| `regtimeTs` | string |  |
| `regtimeUtc` | string |  |
| `state` | string |  |
| `supervisorid` | string |  |
| `timeformat` | string |  |
| `usemfa` | string |  |
| `venmousername` | string |  |
| `weightcapacity` | string |  |
| `wordpressapi` | string |  |
| `wuname` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /workers` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workers.md) for the provider-specific parameters and requirements.

