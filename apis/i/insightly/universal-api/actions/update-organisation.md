# Insightly: Update Organisation

Updates an existing organisation in Insightly.

```
PUT https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-organisation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organisationId": 1,
  "organisationName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightly/latest/actions/update-organisation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organisationId": 1,
    "organisationName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organisationId` | number | yes | The Organisation ID to update. |
| `organisationName` | string | yes | The organisation name. |
| `phone` | string | no | The organisation phone number. |
| `website` | string | no | The organisation website URL. |
| `background` | string | no | Background notes for the organisation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": "string",
      "createdUserId": 1,
      "dateCreatedUtc": "2026-05-07T12:00:00.000Z",
      "dateUpdatedUtc": "2026-05-07T12:00:00.000Z",
      "imageUrl": "https://example.com",
      "lastActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "nextActivityDateUtc": "2026-05-07T12:00:00.000Z",
      "organisationId": 1,
      "organisationName": "Ava Chen",
      "ownerUserId": 1,
      "phone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `background` | string |  |
| `createdUserId` | number |  |
| `dateCreatedUtc` | date |  |
| `dateUpdatedUtc` | date |  |
| `imageUrl` | string |  |
| `lastActivityDateUtc` | date |  |
| `nextActivityDateUtc` | date |  |
| `organisationId` | number |  |
| `organisationName` | string |  |
| `ownerUserId` | number |  |
| `phone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `PUT {{credentials.apiBaseUrl}}Organisations` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-organisation.md) for the provider-specific parameters and requirements.

