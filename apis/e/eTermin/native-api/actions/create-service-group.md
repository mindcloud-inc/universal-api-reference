# Create Service Group with eTermin

Creates a new service group in eTermin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/servicegroup`
- **Base URL:** `https://www.etermin.net`
- **Official documentation:** [Create Service Group](https://app.swaggerhub.com/apis-docs/etermin.net/eTermin-API/1.0.0#/Servicegroup/post_api_servicegroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `servicegroupde` | query | `string` | no | Name of the service group in german. For other languages use servicegroupLANGUAGECODE e.g. servicegroupen |
| `additionaltextde` | query | `string` | no | Additional information of the service group in german. For other languages use additionaltextLANGUAGECODE e.g. additionaltexten |
| `addtextdisplaymode` | query | `number` | no | Defines the location of the additional text (0 = via Tooltip; 1 = under the name of the service group) |
| `servicegrouptype` | query | `number` | no | Defines the service group type (0 = Service selection; 2 = Text field; 5 = location selection; 8 = Day amount selection; 9 = Number search; 10 = Minutes amount selection) |
| `answerselection` | query | `number` | no | Selection type for services (0 = Single selection; 1 = Multi selection; 2 = list selection). Has to be -1 if servicegrouptype is not 0! |
| `isoptional` | query | `boolean` | no | Defines if a selection of a service is mandatory |
| `showprice` | query | `boolean` | no | Defines if the price of the service is shown |
| `showduration` | query | `boolean` | no | Defines if the duration of the service is shown |
| `nrservicecolumns` | query | `number` | no | Defines how many columns the services should be displayed in |
| `showtoggle` | query | `boolean` | no | true if the service group can be collapsed |
| `collapse` | query | `boolean` | no | true if the service group is shown collapsed as default (need showtoggle to be true) |
| `enabled` | query | `boolean` | no | false if the service group should not appear on the bookingpage (only via direct link or for internal services) |
| `showinsummary` | query | `boolean` | no | false if the selected service should not appear in the summary box |
| `showwhencertainanswerselected` | query | `string` | no | List of services that have to be selected to show this service group. Set to -1 if the service group should be shown initially |
