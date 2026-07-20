# Every.org: Create Fundraiser

Creates a new fundraiser in Every.org.

```
POST https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/create-fundraiser
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Every.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/create-fundraiser" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nonprofitId": "string",
  "title": "string",
  "description": "string",
  "goal": 1,
  "raisedOffline": 1,
  "startDate": "string",
  "endDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/create-fundraiser', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nonprofitId": "string",
    "title": "string",
    "description": "string",
    "goal": 1,
    "raisedOffline": 1,
    "startDate": "string",
    "endDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nonprofitId` | string | yes | UUID of the nonprofit supported by the fundraiser. |
| `title` | string | yes | Fundraiser title. |
| `description` | string | yes | Fundraiser description or null. |
| `goal` | number | yes | Goal amount in cents or null. |
| `raisedOffline` | number | yes | Amount raised offline in cents or null. |
| `startDate` | string | yes | ISO-encoded datetime string for when the fundraiser starts or null. |
| `endDate` | string | yes | ISO-encoded datetime string for when the fundraiser ends or null. |
| `imageBase64` | string | no | Optional base64-encoded fundraiser cover image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fundraiser": {
        "active": true,
        "description": "string",
        "goalAmount": "string",
        "goalCurrency": "string",
        "id": "string",
        "nonprofitId": "string",
        "slug": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fundraiser.active` | boolean | Whether the fundraiser is active. |
| `fundraiser.description` | string | Created fundraiser description. |
| `fundraiser.goalAmount` | string | Fundraiser goal amount in cents. |
| `fundraiser.goalCurrency` | string | Fundraiser goal currency. |
| `fundraiser.id` | string | Created fundraiser ID. |
| `fundraiser.nonprofitId` | string | Supported nonprofit ID. |
| `fundraiser.slug` | string | Created fundraiser slug. |
| `fundraiser.title` | string | Created fundraiser title. |

## Native endpoint

Through the native Every.org API, this operation is `POST /fundraiser` (base URL `https://partners.every.org/v0.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-fundraiser.md) for the provider-specific parameters and requirements.

