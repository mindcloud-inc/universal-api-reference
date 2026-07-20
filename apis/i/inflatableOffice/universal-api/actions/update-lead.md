# InflatableOffice: Update Lead

Updates an existing lead in InflatableOffice.

```
PUT https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/update-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/update-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leadId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/update-lead', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leadId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `additionalnotes1` | string | no | Additional notes field 1. |
| `eventname` | string | no | Updated event name for the lead. |
| `leadId` | string | yes | ID of the lead to update. |
| `notes` | string | no | Updated lead notes. |
| `status` | string | no | Updated lead status name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "recordid": "string",
      "requestTime": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `recordid` | string |  |
| `requestTime` | number |  |
| `status` | number |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `POST /leads/:leadId` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead.md) for the provider-specific parameters and requirements.

