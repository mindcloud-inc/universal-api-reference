# Update Service Group with eTermin

Updates an existing service group in eTermin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/servicegroup`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Update Service Group](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/put_api_servicegroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `servicegroupid` | query | `number` | yes | ID of the service group that gets updated |
| `servicegroupde` | query | `string` | no | Name of the service group in german. For other languages use servicegroupLANGUAGECODE e.g. servicegroupen |
| `additionaltextde` | query | `string` | no | Additional information of the service group in german. For other languages use additionaltextLANGUAGECODE e.g. additionaltexten |
| `addtextdisplaymode` | query | `number` | no | Defines the location of the additional text (0 = via Tooltip; 1 = under the name of the service group) |
| `servicegrouptype` | query | `number` | no | Defines the service group type (0 = Service selection; 2 = Text field; 5 = location selection; 8 = Day amount selection; 9 = Number search; 10 = Minutes amount selection) |
| `answerselection` | query | `number` | no | Selection type for services (0 = Single selection; 1 = Multi selection; 2 = list selection). Has to be -1 if servicegrouptype is not 0! |
| `isoptional` | query | `boolean` | no | Defines if a selection of a service is mandatory |
| `showprice` | query | `boolean` | no | Defines if the price of the service is shown |
| `showduration` | query | `boolean` | no | Defines if the duration of the service is shown |
| `nrservicecolumns` | query | `number` | no | Defines how many columns the services should be displayed in |
| `showimgfull` | query | `boolean` | no | true if the picture of the service should be shown as big as possible |
| `showtoggle` | query | `boolean` | no | true if the service group can be collapsed |
| `collapse` | query | `boolean` | no | true if the service group is shown collapsed as default (need showtoggle to be true) |
| `enabled` | query | `boolean` | no | false if the service group should not appear on the bookingpage (only via direct link or for internal services) |
| `answersortorder` | query | `number` | no | Defines in which order the services are shown (0 = according to position in service; 1 = Ascending by name; 2 = Descending by name) |
| `showinsummary` | query | `boolean` | no | false if the selected service should not appear in the summary box |
| `showinemailsummary` | query | `boolean` | no | false if the selected service should not appear in the summary of the emails |
| `pageidx` | query | `number` | no | If set to 1 the service group will be shown on a second service selection page. Default value is 0 |
| `displayindex` | query | `number` | yes | Index in which order the service group should be shown |
| `showwhencertainanswerselected` | query | `string` | no | List of services that have to be selected to show this service group. Set to -1 if the service group should be shown initially |
| `countrylimitation` | query | `string` | no | Languagecodes that are supported by the location lookup (servicegrouptype has to be 5) |
| `regex` | query | `string` | no | Is a validation rule. Can be used if you want to have your location written in a certain way (servicegrouptype has to be 5) |
| `errormsgde` | query | `string` | no | Error message, if the regex isn't valid or a wrong number on the number search is used. For other languages use errormsgLANGUAGECODE e.g. errormsgen (servicegrouptype has to be 5 or 9) |
| `selminduration` | query | `number` | no | The interval of minutes you can switch up or down with the minute selection (servicegrouptype has to be 10) |
| `selminprice` | query | `number` | no | The price of every minute selection interval (servicegrouptype has to be 10) |
