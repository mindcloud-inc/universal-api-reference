# Raisely: Update Profile

Updates an existing profile in Raisely.

```
PUT https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-profile', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | no | The `uuid`, `path` or domain of the campaign to associate with the request |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `partial` | boolean | no | Determines if a record updates public/private values in a merge verses an overwrite |
| `data` | object | no |  |
| `data.currency` | string | no | 3 letter currency code Examples: `AUD`, `USD` |
| `data.description` | string | no | Public description of the fundraiser profile Example: `I believe in a better world` |
| `data.exerciseGoal` | number | no | The exercise distance goal for the profile, in metres Example: `12345` |
| `data.exerciseGoalTime` | number | no | The time spent exercising goal for the profile, in minutes Example: `12345` |
| `data.fundraiserTheme` | string | no | Path of the DIY fundraiser theme selected by the fundraiser Examples: `birthday`, `bake-sale` |
| `data.goal` | number | no | Fundraising target (in cents) Example: `100050` |
| `data.name` | string | no | The name of the profile Example: `Bob D.` |
| `data.path` | string | no | The path of this record (for alternative lookup) Example: `bobd` |
| `data.photoUrl` | string | no | URL of the profile photo Example: `https://raisely-images.imgix.net/www/uploads/t-03-arl-8-es-uhhqua-4-pr-f-4865431-df-58-512-png-08e3f5.png` |
| `data.private` | object | no | Private values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.pronouns` | string | no | Pronouns of the profile |
| `data.public` | object | no | Public values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.type` | string | no | INDIVIDUAL, GROUP or ORGANISATION Examples: `INDIVIDUAL`, `GROUP`, `ORGANISATION` |
| `overwriteCustomFields` | boolean | no | If passed, replace the existing `public` and `private` values on the record with the values provided with this payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityTotal": 1,
      "campaignTotal": 1,
      "campaignUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "description": "string",
      "exerciseTotal": 1,
      "exerciseTotalTime": 1,
      "feeTotal": 1,
      "goal": 1,
      "grandTotal": 1,
      "name": "Ava Chen",
      "nonSelfDonationTotal": 1,
      "paid": true,
      "path": "string",
      "photoUrl": "https://example.com",
      "selfDonationTotal": 1,
      "status": "string",
      "total": 1,
      "totalPercent": 1,
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityTotal` | number |  |
| `campaignTotal` | number |  |
| `campaignUuid` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `description` | string |  |
| `exerciseTotal` | number |  |
| `exerciseTotalTime` | number |  |
| `feeTotal` | number |  |
| `goal` | number |  |
| `grandTotal` | number |  |
| `name` | string |  |
| `nonSelfDonationTotal` | number |  |
| `paid` | boolean |  |
| `path` | string |  |
| `photoUrl` | string |  |
| `selfDonationTotal` | number |  |
| `status` | string |  |
| `total` | number |  |
| `totalPercent` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `PATCH /profiles/:path` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-profile.md) for the provider-specific parameters and requirements.

