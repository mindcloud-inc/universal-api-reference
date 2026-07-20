# Create Job with VSCO Workspace

Creates a new job in VSCO Workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/job`
- **Base URL:** `https://workspace.vsco.co/api/v2`
- **Official documentation:** [Create Job](https://workspace.vsco.co/api/#operation/createResourceJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `brandId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `closed` | body | `boolean` | no | Whether or not the lead or job is closed. A closed reason might be provided as well. |
| `closedReasonId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `closedDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `completedDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `contactFormId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `customFields[]` | body | `array<object>` | no | — |
| `eventDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `fulfillmentDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `guestCount` | body | `number` | no | — |
| `inquiryDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `jobTypeId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `lastClientActivity` | body | `object` | no | — |
| `leadConfidence` | body | `string` | no | — |
| `leadDecisionExpectedByDate` | body | `date` | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `leadMaxBudget` | body | `number` | no | — |
| `leadNotes` | body | `string` | no | — |
| `leadRating` | body | `number` | no | — |
| `leadSourceId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `leadStatusId` | body | `string` | no | A ULID entity identifier that is nullable. |
| `leadStatusChangedAt` | body | `object` | no | — |
| `name` | body | `string` | no | Name of the job that will override the title. |
| `nextInteractionDate` | body | `object` | no | — |
| `pinned` | body | `boolean` | no | — |
| `primarySessionId` | body | `object` | no | — |
| `previousInteractionDate` | body | `object` | no | — |
| `stage` | body | `string` | no | Specifies the stage that the job is in. |
| `staleDate` | body | `object` | no | — |
| `totalCost` | body | `object` | no | — |
| `totalProfit` | body | `object` | no | — |
| `totalRevenue` | body | `object` | no | — |
| `webLead` | body | `boolean` | no | Whether or not the lead or job came from a contact form. |
| `workflowId` | body | `string` | no | A ULID entity identifier that is nullable. |
