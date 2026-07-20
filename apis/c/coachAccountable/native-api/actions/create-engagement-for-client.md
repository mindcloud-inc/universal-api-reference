# Create Engagement for Client with CoachAccountable

Creates a client engagement in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Engagement for Client](https://www.coachaccountable.com/APIDocs#Engagement.addForClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client for whom the Engagement is to be added. |
| `EngagementTemplateID` | body | `number` | yes | The ID of the Engagement Template to be used to fill in the details of the new Engagement. |
| `startDate` | body | `date` | no | The date that the Engagement is to begin. Defaults to today if not provided. |
| `endDate` | body | `date` | no | The date that the Engagement is to end. Defaults to the end date implied by the Engement Template's duration setting, either bounded or indefinite. |
| `allocation` | body | `string` | no | The initial allocation of the Engagement expressed as a number followed by a space followed by the unit, either "A" for Appointments or "H" for hours (e.g. "12 A" or "6 H"). Defaults to the value given by the Engement Template. |
| `initializeInvoices` | body | `boolean` | no | Setting this to true CAN trigger the immediate creation of one or more invoices. If the Client has a card on file that allows automatic billing, that can result in immediate charges. When false, no invoices will be sent for the Engagement until manually configured by editing the Engagement in-app. |
| `allowMultipleCurrentEngagements` | body | `boolean` | no | Having a client be in multiple Engagements that overlap in time is USUALLY a bad idea. Set this to true to allow it anyway, otherwise CA will return a 440 error when it detects that adding this Engagement would cause an overlap. |
