# Pledge: Create Fundraiser

Creates a fundraiser in Pledge.

```
POST https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-fundraiser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-fundraiser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "beneficiary.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pledge/latest/actions/create-fundraiser', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "beneficiary.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beneficiary.id` | string | yes | Organization ID for the fundraiser beneficiary. |
| `goal` | string | no | Fundraising goal amount. |
| `startTime` | string | no | Event start time in ISO 8601 format. |
| `endTime` | string | no | Event end time in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeDonors": 1,
      "activeRaised": "string",
      "beneficiary": {
        "alias": "string",
        "cause": "string",
        "causes": [
          {
            "id": 1,
            "name": "Ava Chen",
            "parentId": {}
          }
        ],
        "city": "string",
        "country": "string",
        "disbursementType": "string",
        "id": "string",
        "lat": "string",
        "logoUrl": "https://example.com",
        "lon": "string",
        "mission": "string",
        "name": "Ava Chen",
        "ngoId": "string",
        "postalCode": "string",
        "profileUrl": "https://example.com",
        "region": "string",
        "street1": "string",
        "street2": "string",
        "sustainableDevelopmentGoals": [
          {
            "id": 1,
            "name": "Ava Chen"
          }
        ],
        "type": "string",
        "websiteUrl": "https://example.com"
      },
      "createdAt": "string",
      "deletedAt": {},
      "endTime": {},
      "eventType": {},
      "goal": "string",
      "id": "string",
      "invitationType": {},
      "name": {},
      "overlayUrl": {},
      "startTime": {},
      "totalDonors": 1,
      "totalRaised": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "zipCode": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeDonors` | number |  |
| `activeRaised` | string |  |
| `beneficiary.alias` | string |  |
| `beneficiary.cause` | string |  |
| `beneficiary.causes[].id` | number |  |
| `beneficiary.causes[].name` | string |  |
| `beneficiary.causes[].parentId` | object |  |
| `beneficiary.city` | string |  |
| `beneficiary.country` | string |  |
| `beneficiary.disbursementType` | string |  |
| `beneficiary.id` | string |  |
| `beneficiary.lat` | string |  |
| `beneficiary.logoUrl` | string |  |
| `beneficiary.lon` | string |  |
| `beneficiary.mission` | string |  |
| `beneficiary.name` | string |  |
| `beneficiary.ngoId` | string |  |
| `beneficiary.postalCode` | string |  |
| `beneficiary.profileUrl` | string |  |
| `beneficiary.region` | string |  |
| `beneficiary.street1` | string |  |
| `beneficiary.street2` | string |  |
| `beneficiary.sustainableDevelopmentGoals[].id` | number |  |
| `beneficiary.sustainableDevelopmentGoals[].name` | string |  |
| `beneficiary.type` | string |  |
| `beneficiary.websiteUrl` | string |  |
| `createdAt` | string |  |
| `deletedAt` | object |  |
| `endTime` | object |  |
| `eventType` | object |  |
| `goal` | string |  |
| `id` | string |  |
| `invitationType` | object |  |
| `name` | object |  |
| `overlayUrl` | object |  |
| `startTime` | object |  |
| `totalDonors` | number |  |
| `totalRaised` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `zipCode` | object |  |

## Native endpoint

Through the native Pledge API, this operation is `POST /fundraisers` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fundraiser.md) for the provider-specific parameters and requirements.

