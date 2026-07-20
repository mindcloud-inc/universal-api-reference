# eTermin: Create Service Group

Creates a new service group in eTermin.

```
POST https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-service-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-service-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/create-service-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `servicegroupde` | string | no | Name of the service group in german. For other languages use servicegroupLANGUAGECODE e.g. servicegroupen |
| `additionaltextde` | string | no | Additional information of the service group in german. For other languages use additionaltextLANGUAGECODE e.g. additionaltexten |
| `addtextdisplaymode` | number | no | Defines the location of the additional text (0 = via Tooltip; 1 = under the name of the service group) |
| `servicegrouptype` | number | no | Defines the service group type (0 = Service selection; 2 = Text field; 5 = location selection; 8 = Day amount selection; 9 = Number search; 10 = Minutes amount selection) |
| `answerselection` | number | no | Selection type for services (0 = Single selection; 1 = Multi selection; 2 = list selection). Has to be -1 if servicegrouptype is not 0! |
| `isoptional` | boolean | no | Defines if a selection of a service is mandatory |
| `showprice` | boolean | no | Defines if the price of the service is shown |
| `showduration` | boolean | no | Defines if the duration of the service is shown |
| `nrservicecolumns` | number | no | Defines how many columns the services should be displayed in |
| `showtoggle` | boolean | no | true if the service group can be collapsed |
| `collapse` | boolean | no | true if the service group is shown collapsed as default (need showtoggle to be true) |
| `enabled` | boolean | no | false if the service group should not appear on the bookingpage (only via direct link or for internal services) |
| `showinsummary` | boolean | no | false if the selected service should not appear in the summary box |
| `showwhencertainanswerselected` | string | no | List of services that have to be selected to show this service group. Set to -1 if the service group should be shown initially |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "status": 1,
      "statusmsg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `status` | number |  |
| `statusmsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `POST /api/servicegroup` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-group.md) for the provider-specific parameters and requirements.

