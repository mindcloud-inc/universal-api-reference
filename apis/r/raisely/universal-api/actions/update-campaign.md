# Raisely: Update Campaign

Updates an existing campaign in Raisely.

```
PUT https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/raisely/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaign` | string | yes | The `uuid`, `path` or domain of the campaign to associate with the request |
| `data` | object | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.allowExperiments` | boolean | no | Allows the campaign to participate in Raisely experiments Examples: `true`, `false` |
| `data.currency` | string | no | 3 letter currency code Examples: `AUD`, `USD` |
| `data.defaultCampaignFund` | string | no | Fund that is assigned as the default fund for the campaign |
| `data.goal` | number | no | (in cents) Example: `500050` |
| `data.mode` | string | no | Mode for payment processing. Make sure to set this to LIVE before launching your campaign so you can take real donations. Examples: `LIVE`, `TEST` |
| `data.name` | string | no | Name of the campaign Example: `<< campaign name >>` |
| `data.path` | string | no | The path of this record (for alternative lookup) Example: `run-for-a-cure` |
| `data.primaryDomain` | string | no | Primary domain of the campaign |
| `data.private` | object | no | Private values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.public` | object | no | Public values for this record Example: `{ "fieldA": "one", "fieldB": "yes" }` |
| `data.publicKey` | string | no | (Internal Raisely field - ignored) Example: `aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa` |
| `data.theme` | string | no | The theme name by this campaign Examples: `donation-basic`, `donation-modern`, `donation-elegant`, `donation-expansive`, `donation-impact`, `donation-elegant`, `donation-active`, `peerToPeer-basic`, `peerToPeer-modern`, `peerToPeer-elegant`, `peerToPeer-expansive`, `peerToPeer-impact`, `peerToPeer-elegant`, `peerToPeer-active`, `appealsHub-basic`, `appealsHub-modern`, `appealsHub-elegant`, `appealsHub-expansive`, `appealsHub-impact`, `appealsHub-elegant`, `appealsHub-active`, `communityHub-basic`, `communityHub-modern`, `communityHub-elegant`, `communityHub-expansive`, `communityHub-impact`, `communityHub-elegant`, `communityHub-active`, `appeal-basic`, `appeal-modern`, `appeal-elegant`, `appeal-expansive`, `appeal-impact`, `appeal-elegant`, `appeal-active`, `special-virtualEvent`, `special-virtualAppeal`, `special-charityChallenge` |
| `data.urls[]` | array<string> | no | Custom domains of the campaign Example: `[ "yourdomain.com" ]` |
| `data.urls[]` | array<string> | no | Custom domains of the campaign Example: `[ "yourdomain.com" ]` |
| `data.version` | string | no | Theme version Example: `3.0.0` |
| `overwriteCustomFields` | boolean | no | If passed, replace the existing `public` and `private` values on the record with the values provided with this payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowExperiments": true,
      "currency": "string",
      "defaultCampaignFund": "string",
      "goal": 1,
      "mode": "string",
      "name": "Ava Chen",
      "path": "string",
      "primaryDomain": "string",
      "private": {},
      "public": {},
      "publicKey": "string",
      "theme": "string",
      "urls": [
        "https://example.com"
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowExperiments` | boolean |  |
| `currency` | string |  |
| `defaultCampaignFund` | string |  |
| `goal` | number |  |
| `mode` | string |  |
| `name` | string |  |
| `path` | string |  |
| `primaryDomain` | string |  |
| `private` | object |  |
| `public` | object |  |
| `publicKey` | string |  |
| `theme` | string |  |
| `urls` | array<string> |  |
| `version` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `PATCH /campaigns/:campaign` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

