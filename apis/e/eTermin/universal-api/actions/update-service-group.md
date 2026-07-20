# eTermin: Update Service Group

Updates an existing service group in eTermin.

```
PUT https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-service-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eTermin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-service-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "servicegroupid": 1,
  "displayindex": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eTermin/latest/actions/update-service-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "servicegroupid": 1,
    "displayindex": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `servicegroupid` | number | yes | ID of the service group that gets updated |
| `servicegroupde` | string | no | Name of the service group in german. For other languages use servicegroupLANGUAGECODE e.g. servicegroupen |
| `additionaltextde` | string | no | Additional information of the service group in german. For other languages use additionaltextLANGUAGECODE e.g. additionaltexten |
| `addtextdisplaymode` | number | no | Defines the location of the additional text (0 = via Tooltip; 1 = under the name of the service group) |
| `servicegrouptype` | number | no | Defines the service group type (0 = Service selection; 2 = Text field; 5 = location selection; 8 = Day amount selection; 9 = Number search; 10 = Minutes amount selection) |
| `answerselection` | number | no | Selection type for services (0 = Single selection; 1 = Multi selection; 2 = list selection). Has to be -1 if servicegrouptype is not 0! |
| `isoptional` | boolean | no | Defines if a selection of a service is mandatory |
| `showprice` | boolean | no | Defines if the price of the service is shown |
| `showduration` | boolean | no | Defines if the duration of the service is shown |
| `nrservicecolumns` | number | no | Defines how many columns the services should be displayed in |
| `showimgfull` | boolean | no | true if the picture of the service should be shown as big as possible |
| `showtoggle` | boolean | no | true if the service group can be collapsed |
| `collapse` | boolean | no | true if the service group is shown collapsed as default (need showtoggle to be true) |
| `enabled` | boolean | no | false if the service group should not appear on the bookingpage (only via direct link or for internal services) |
| `answersortorder` | number | no | Defines in which order the services are shown (0 = according to position in service; 1 = Ascending by name; 2 = Descending by name) |
| `showinsummary` | boolean | no | false if the selected service should not appear in the summary box |
| `showinemailsummary` | boolean | no | false if the selected service should not appear in the summary of the emails |
| `pageidx` | number | no | If set to 1 the service group will be shown on a second service selection page. Default value is 0 |
| `displayindex` | number | yes | Index in which order the service group should be shown |
| `showwhencertainanswerselected` | string | no | List of services that have to be selected to show this service group. Set to -1 if the service group should be shown initially |
| `countrylimitation` | string | no | Languagecodes that are supported by the location lookup (servicegrouptype has to be 5) |
| `regex` | string | no | Is a validation rule. Can be used if you want to have your location written in a certain way (servicegrouptype has to be 5) |
| `errormsgde` | string | no | Error message, if the regex isn't valid or a wrong number on the number search is used. For other languages use errormsgLANGUAGECODE e.g. errormsgen (servicegrouptype has to be 5 or 9) |
| `selminduration` | number | no | The interval of minutes you can switch up or down with the minute selection (servicegrouptype has to be 10) |
| `selminprice` | number | no | The price of every minute selection interval (servicegrouptype has to be 10) |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `status` | number |  |
| `statusmsg` | string |  |

## Native endpoint

Through the native eTermin API, this operation is `PUT /api/servicegroup` (base URL `https://www.etermin.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service-group.md) for the provider-specific parameters and requirements.

