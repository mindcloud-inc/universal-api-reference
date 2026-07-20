# Better Proposals: Create Proposal Cover

Creates a proposal cover in Better Proposals.

```
POST https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-proposal-cover
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Proposals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-proposal-cover" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterProposals/latest/actions/create-proposal-cover', {
  method: 'POST',
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
| `brandId` | string | no | Brand ID. If omitted, Better Proposals uses the brand settings defaults. |
| `coverName` | string | no | Cover name. Default is Untitled. Default: `Untitled`. |
| `bgColour` | string | no | Background colour value. Default is 111111. Default: `111111`. |
| `headline` | string | no | Cover headline. Default is Proposal for _________. Default: `Proposal for _________`. |
| `subheader` | string | no | Cover subheader. Default is Written by ________ for ________. Default: `Written by ________ for ________`. |
| `textColour` | string | no | Text colour value. Default is ffffff. Default: `ffffff`. |
| `textAlign` | string | no | Text alignment. Default is left. Default: `left`. |
| `buttonStyle` | string | no | Button style. Default is round. Default: `round`. |
| `buttonText` | string | no | Button text. Default is Start Reading Proposal. Default: `Start Reading Proposal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountID": "string",
      "bGColour": "string",
      "bGFilter": "string",
      "bGImageThumb": {},
      "brandID": "string",
      "buttonStyle": "string",
      "buttonText": "string",
      "createdBy": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateEdited": "2026-05-07T12:00:00.000Z",
      "deleted": "string",
      "editedBy": "string",
      "headline": "string",
      "id": "string",
      "logo": "string",
      "name": "Ava Chen",
      "subheader": "string",
      "textAlign": "string",
      "textColour": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `bGColour` | string |  |
| `bGFilter` | string |  |
| `bGImageThumb` | object |  |
| `brandID` | string |  |
| `buttonStyle` | string |  |
| `buttonText` | string |  |
| `createdBy` | string |  |
| `dateCreated` | date |  |
| `dateEdited` | date |  |
| `deleted` | string |  |
| `editedBy` | string |  |
| `headline` | string |  |
| `id` | string |  |
| `logo` | string |  |
| `name` | string |  |
| `subheader` | string |  |
| `textAlign` | string |  |
| `textColour` | string |  |

## Native endpoint

Through the native Better Proposals API, this operation is `POST /proposal/cover/create` (base URL `https://api.betterproposals.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-proposal-cover.md) for the provider-specific parameters and requirements.

