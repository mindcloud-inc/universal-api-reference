# Create Time Card with ADP

## Endpoint

- **Method:** `POST`
- **Path:** `events/time/v2/time-entries.modify`
- **Base URL:** `https://api.adp.com/`
- **Official documentation:** [Create Time Card](https://developers.adp.com/apis/api-explorer/hcm-offrg-wfn/hcm-offrg-wfn-time-time-cards-v2-time-cards?operation=POST%2Fevents%2Ftime%2Fv2%2Ftime-entries.modify#swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `associateOID` | body | `string` | no | — |
| `workAssignmentID` | body | `string` | no | — |
| `startTime` | body | `date` | no | — |
| `endTime` | body | `date` | no | — |
| `entryTypeCode` | body | `list<string>` | no | - dayPeriodEntry -> Used for employee whose the presence is declared in day period (morning, afternoon, fullday). - hoursEntry -> Used for employee whose the presence is declared in duration. - timePairEntry -> Used for employee whose the presence is declared in slice time. |
| `duration` | body | `number` | no | indicate how many minutes were worked. INT -> 150 = 2 hours and 30 minutes |
| `dayPeriodCode` | body | `list<string>` | no | — |
| `entryCode` | body | `string` | no | what type of entry is being saved (service, meal, shop, tip, etc) |
