# CoachAccountable: Create Engagement for Client

Creates a client engagement in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-engagement-for-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-engagement-for-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "engagementTemplateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/create-engagement-for-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "engagementTemplateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes | The ID of the Client for whom the Engagement is to be added. |
| `engagementTemplateId` | number | yes | The ID of the Engagement Template to be used to fill in the details of the new Engagement. |
| `startDate` | date | no | The date that the Engagement is to begin. Defaults to today if not provided. |
| `endDate` | date | no | The date that the Engagement is to end. Defaults to the end date implied by the Engement Template's duration setting, either bounded or indefinite. |
| `allocation` | string | no | The initial allocation of the Engagement expressed as a number followed by a space followed by the unit, either "A" for Appointments or "H" for hours (e.g. "12 A" or "6 H"). Defaults to the value given by the Engement Template. |
| `initializeInvoices` | boolean | no | Setting this to true CAN trigger the immediate creation of one or more invoices. If the Client has a card on file that allows automatic billing, that can result in immediate charges. When false, no invoices will be sent for the Engagement until manually configured by editing the Engagement in-app. Default: `false`. |
| `allowMultipleCurrentEngagements` | boolean | no | Having a client be in multiple Engagements that overlap in time is USUALLY a bad idea. Set this to true to allow it anyway, otherwise CA will return a 440 error when it detects that adding this Engagement would cause an overlap. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "EngagementID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `EngagementID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-engagement-for-client.md) for the provider-specific parameters and requirements.

